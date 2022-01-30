# Nmap
## Examples
### Basic SMB vuln scan (WARNING: DANGEROUS!!!)
```
sudo nmap --script=smb-check-vulns.nse $IP
```
### Basic SMB vuln scan with unsafe scripts
```
nmap –script smb-check-vulns.nse –script-args=unsafe=1 $IP
```
### Basic SMB vuln scan with (supposedly) safe scripts
```
nmap –script smb-check-vulns.nse –script-args=safe=1 $IP
```
### Do all smb vuln scan for scripts starting with `smb-vuln` using wildcard
```
sudo nmap -T4 -sS -sC -Pn -A --script smb-vuln* $IP
```
### Explicit script blanket enumeration
```
nmap --script smb-enum-domains.nse,smb-enum-groups.nse,smb-enum-processes.nse,smb-enum-services.nse,smb-enum-sessions.nse,smb-enum-shares.nse,smb-enum-users.nse -p445 $IP
```
### Explicit blanket script vulnerability exploit
```
nmap --script smb-vuln-conficker.nse,smb-vuln-cve2009-3103.nse,smb-vuln-cve-2017-7494.nse,smb-vuln-ms06-025.nse,smb-vuln-ms07-029.nse,smb-vuln-ms08-067.nse,smb-vuln-ms10-054.nse,smb-vuln-ms10-061.nse,smb-vuln-ms17-010.nse,smb-vuln-regsvc-dos.nse,smb-vuln-webexec.nse -p445 $IP
```