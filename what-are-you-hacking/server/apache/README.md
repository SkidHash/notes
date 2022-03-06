# Apache
## Viewing all files with same names but different extensions
If Apache mod_negotiation is enabled with MultiViews you can brute force file names
https://www.wisec.it/sectou.php?id=4698ebdc59d15

Basically you can make a request and replace the `Accept` header with the following:
```
Accept: application/whatever;q=1.0
```
And make a request to any file (in this example, index):
```
http://TARGET_IP/index
```

And you will get a response back listing all files that match index
```
// other text
index.php
index.bak
index.html
```