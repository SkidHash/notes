# Common
## Directory Location
### ssh
```
/home/$user/.ssh/id_rsa
```
### common file everyone can read
#### /etc/passwd
```
/etc/passwd
```
### cron
#### view current cronjobs
```
cat /etc/crontab
```
#### other cron directory
```
/var/spool/cron/crontab
```
#### root cron config file
```
/var/spool/cron/crontab/root
```
## Sudo
### check for who has sudo
#### sudo history
```
# which users have recently used sudo
cat /var/log/auth.log
```
#### who can use sudo
```
#Check sudoers file
cat /etc/sudoers
```