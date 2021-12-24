# gobuster
## Examples
### brute forcing directories
```
$> gobuster -u http://ip -w /usr/share/seclists/Discovery/Web_Content/common.txt
```
### brute forcing only accept certain status codes on return
```
$> gobuster -u http://ip -w /usr/share/seclists/Discovery/Web_Content/common.txt -s '200,204,301,302,307,403,500' -e
```
