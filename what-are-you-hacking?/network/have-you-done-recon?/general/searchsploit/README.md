# searchsploit
## 
## Examples
###  Using an nmap scan
```
searchsploit --nmap nmap_scan_output.xml
```

###  Basic query for keyword
```
searchsploit keyword
```
### Basic query for keyword + version
```
searchsploit keyword version
```

### Show and Copy exploit path to clipboard
the path from a previous query was `windows_x86/local/$EXPLOIT_NUM.py`
```
searchsploit -p $EXPLOIT_NUM
```

###  Copy exploit file to local folder
```
searchsploit -m $EXPLOIT_NUM_A win_x86-64/local/$EXPLOIT_NUM_B.py
```
Copies $EXPLOIT_NUM_A and $EXPLOIT_NUM_B to the current folder

###  Lookup exploitdb URL
```
searchsploit keyword -w # https://www.exploit-db.com/exploits/$EXPLOIT_NUM_A
```

###  Update local searchsploit db
```
searchsploit --update
```