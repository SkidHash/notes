# ftp
## Examples
### FTP to an IP and port
```
$> ftp -v $IP $port
Connected to $IP
220 ProFTPD Server Debian
Name (myIP:kali): anonymous
331 Anonymous login ok, send your complete email address as your password
Password:
230-Welcome, archive user anonymous@myIP !
230-
230-The local time is: Thu Oct 28 20:38:59 2021
230-
230 Anonymous access granted, restrictions apply
Remote system type is UNIX
Using binary mode to transfer files.
ftp>
```
Anonymous login means the following
> username is 'anonymous'
> password is anything

`-v` is the verbose flag

The default port if `$port` is left out is 21
