# dirsearch
https://github.com/maurosoria/dirsearch
## Examples
### Brute forcing directories of an IP address
```
$> dirsearch -u $IP
```
### recursively brute forcing directories of an IP address
```
$> dirsearch -u $IP -r
```
### brute forcing only accept certain codes on return
```
$> dirsearch -u $IP --exclude-status=301,400-499,500-599
```
### brute force for certain extensions
```
$> dirsearch -u $IP -e php
```
### brute force with custom wordlist
```
$> dirsearch -u $IP -w /usr/share/wordlist/rockyou.txt
```
### recursively brute force ignoring certain status codes
```
$> dirsearch -u $IP -r --exclude-status=301,400-499,500-599
```
