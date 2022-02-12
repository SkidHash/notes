# ip
## Examples
### view arp
```
ip n
```
##### Successful output
```
┌──(kali㉿kali)-[~]
└─$ ip n
172.16.210.2 dev eth0 lladdr 00:50:56:f8:fa:a5 REACHABLE
                                                                                                                                               
┌──(kali㉿kali)-[~]
└─$
```
### view routing tables
```
ip r
```
##### Successful output
```
┌──(kali㉿kali)-[~]
└─$ ip r    
default via 172.16.210.2 dev eth0 proto dhcp metric 100 
172.16.210.0/24 dev eth0 proto kernel scope link src 172.16.210.128 metric 100 
                                                                                                                                               
┌──(kali㉿kali)-[~]
└─$
```