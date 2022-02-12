# Enumeration
Scan with the following tools:
1.  nmap
1.  nikto
1.  enum4linux

Throw the results of nmap into searchsploit

##  Result Analysis
###  What did you find?
<details>
<summary>FTP</summary>

#### FTP

##### TFTP
##### SFTP

</details>

<details>
<summary>Website</summary>

#### Website
##### sub domains
1.  Try sublist3r or crt.sh or equivalent to list subdomains
1.  Look for internal dev/stage domains
    1.  also look for dev stuff like bitbucket or github
    1.  sso domains
1.  try poking sensitive subdomains
    1.  tomnomnom httpprobe
    1.  nmap ping scan

##### webserver tech stack
1.  Try looking on https://builtwith.com
1.  Try looking at wappalyzer

</details>

</details>

<details>
<summary>Active Directory</summary>

#### Active Directory

</details>
