# rpcclient
## Flags
### -U
username
### -N
IP of host
### --pw-nt-hash
Format credentials as NT hash

## Examples
### Null/anonymous session
```
rpcclient -U "" -N $IP
```

### 
```
rpcclient //$IP -U domain/$USERNAME%$NTLM_HASH --pw-nt-hash
```