# SMBMap
## Examples
### Enumerating Share Drives Across a Domain with a Username and Password
```
$> sudo smbmap -u $username -p $password -H $IP
```
### Finding all shares without auth and open directories
```
while read i; do smbmap -H $IP 2>/dev/null; done < <Target IP File> | grep -v Finding | grep -v Authentication
```
### Login using NTLM hash
```
smbmap -u "username" -p "<NT>:<LM>" -H $IP
```
### Enumerate as unauthenticated user
```
smbmap -H $IP
```
### Enumerate a disk/share's directory (non recursive)
```
smbmap -u "username" -p "password" -r [Folder] -H $IP
```
### Enumerate a disk/share's directory (recursive) (time consuming)
```
smbmap -u "username" -p "password" -R [Folder] -H $IP
```