# THC Hydra
## Description
Brute force login.  This is for brute forcing ssh

Default port is 22 in all cases unless specified
## Examples
### Brute force SSH for several users with rockyou.txt password list
```
sudo hydra -L users.txt -P /usr/share/wordlists/rockyou.txt $IP ssh
```
### Brute force SSH for single user with rockyou.txt password list
```
sudo hydra -l $USERNAME -P /usr/share/wordlists/rockyou.txt $IP ssh
```
### Brute force SSH for users with known password
```
sudo hydra -L $user_list -p $password $IP ssh
```
### Brute force SSH on a different port
```
sudo hydra -s $port_number -L $user_list -p $password $IP ssh
```
