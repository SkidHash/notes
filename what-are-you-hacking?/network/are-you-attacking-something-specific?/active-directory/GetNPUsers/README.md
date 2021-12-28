# GetNPUsers.py
from impacket
## Examples
### get users without auth
```
GETNPUsers.py $DOMAIN_NAME_FROM_SCAN/ -dc-ip $IP -no-pass -usersfile /
```
### Get all users in AD
```
GETNPUsers.py $DOMAIN_NAME_FROM_SCAN/ -dc-ip $IP -debug
```