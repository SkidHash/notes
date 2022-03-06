# nmap
## Examples
### Check if FTP server allows anonymous logins via script
```
nmap -p $port --script ftp-anon $IP
```
### brute force password auditing against FTP servers
```
nmap -p $port --script ftp-brute $IP
```
### Checks to see if port scannign is allowed through FTP bounce method
```
nmap -p $port --script ftp-bounce $IP
```
