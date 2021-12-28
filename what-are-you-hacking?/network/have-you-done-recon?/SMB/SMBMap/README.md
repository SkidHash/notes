# SMBMap
## Examples
### Enumerating Share Drives Across a Domain with a Username and Password
```
$> sudo smbmap -u $username -p $password -H $IP
```
### Finding all shares without auth and open directories
```
while read i; do smbmap -H $i 2>/dev/null; done < <Target IP File> | grep -v Finding | grep -v Authentication
```