# arp-scan
## Examples
### Get all IPs and MAC on network
```
sudo arp-scan -l
```
#### Successful Output
```
┌──(kali㉿kali)-[~]
└─$ sudo arp-scan -l
Interface: eth0, type: EN10MB, MAC: 00:0c:29:e5:a8:51, IPv4: 172.16.210.133
Starting arp-scan 1.9.7 with 256 hosts (https://github.com/royhills/arp-scan)
172.16.210.1    <Sensitive MAC Address because host machine>       (Unknown: locally administered)
172.16.210.2    <my kali vm mac>       VMware, Inc.
172.16.210.254  <my kali vm mac>       VMware, Inc.

3 packets received by filter, 0 packets dropped by kernel
Ending arp-scan 1.9.7: 256 hosts scanned in 1.971 seconds (129.88 hosts/sec). 3 responded
                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ 
```

#### Bad Output
```
```

### 
