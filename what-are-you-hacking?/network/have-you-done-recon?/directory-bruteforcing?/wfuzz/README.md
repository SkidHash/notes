# wfuzz
## Examples
### scan an IP with wordlist looking for files
```
$> wfuzz -c -z file,/usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt --sc 200 $IP
```
