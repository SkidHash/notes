# dirb
## Examples
### Basic Scan
```
$> sudo dirb $IP
```
### Basic Scan with Modified Header (bypass WAF)
```
$> dirb http://target.com -a "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome 51.0.2704.106 Safari/537.36"
```
#### Flags
##### -a
Lets you change the request header.  This is useful when you are getting 403 errors instead of 404 errors.  It might mean there is a web application firewall (WAF) and so in order to bypass you will need to change your headers
