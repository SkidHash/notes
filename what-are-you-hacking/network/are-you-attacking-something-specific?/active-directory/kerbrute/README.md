# kerbrute
## Examples
### enumerate users via kerberos
```
kerbrute userenum -d $IP  --dc $dc_IP users.txt
```
#### Example
##### Successful username enumeration
```

```

##### Bad Domain, Failed to enumerate
```
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ kerbrute userenum -d spookysec.local0. --dc $IP user_list.txt                                                      1 ⨯

    __             __               __     
   / /_____  _____/ /_  _______  __/ /____ 
  / //_/ _ \/ ___/ __ \/ ___/ / / / __/ _ \
 / ,< /  __/ /  / /_/ / /  / /_/ / /_/  __/
/_/|_|\___/_/  /_.___/_/   \__,_/\__/\___/                                        

Version: dev (n/a) - 02/12/22 - Ronnie Flathers @ropnop

2022/02/12 10:10:35 >  Using KDC(s):
2022/02/12 10:10:35 >   10.10.213.211:88

2022/02/12 10:10:36 >  [!] info@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] robert@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] NULL@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] admin@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] john@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] michael@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] david@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] 2000@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] mike@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] chris@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] richard@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] 123456@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] thomas@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] dave@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] svc-azure@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] daniel@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] andrew@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] mark@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] george@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] steve@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  [!] paul@spookysec.local0. - KDC ERROR - Wrong Realm. Try adjusting the domain? Aborting...
2022/02/12 10:10:36 >  Done! Tested 21 usernames (0 valid) in 0.427 seconds
                                                                                                                           
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ 
```

### enumerate users without domain controller IP
```
kerbrute userenum -d $DNS user_list.txt
```
This will look up the domain via DNS.  If an IP is supplied you may also need to supply the domain controller IP
#### Example
```
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ kerbrute userenum -d $IP user_list.txt 

    __             __               __     
   / /_____  _____/ /_  _______  __/ /____ 
  / //_/ _ \/ ___/ __ \/ ___/ / / / __/ _ \
 / ,< /  __/ /  / /_/ / /  / /_/ / /_/  __/
/_/|_|\___/_/  /_.___/_/   \__,_/\__/\___/                                        

Version: dev (n/a) - 02/12/22 - Ronnie Flathers @ropnop

2022/02/12 09:56:42 >  Couldn't find any KDCs for realm 10.10.213.211. Please specify a Domain Controller
                                                                                                                           
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$
```