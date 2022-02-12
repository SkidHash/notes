# arp
## Examples
### See MAC and IP of other machines on network
```
arp -a
```
#### Successful Output
```
┌──(kali㉿kali)-[~]
└─$ arp -a
? (172.16.210.2) at 00:50:56:f8:fa:a5 [ether] on eth0
                                                                                                                                               
┌──(kali㉿kali)-[~]
└─$
```

### Display ARP information
```
arp
```
#### Successful output
```
┌──(kali㉿kali)-[~]
└─$ arp                   
Address                  HWtype  HWaddress           Flags Mask            Iface
172.16.210.2             ether   00:50:56:f8:fa:a5   C                     eth0
                                                                                                                                               
┌──(kali㉿kali)-[~]
└─$
```