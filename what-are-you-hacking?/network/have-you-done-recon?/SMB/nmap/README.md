# Nmap
## Examples
### Basic SMB vuln scan (WARNING: DANGEROUS!!!)
```
$> sudo nmap --script=smb-check-vulns.nse $IP
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
$> sudo nmap -T4 -sS -sC -Pn -A --script smb-vuln* $IP
```
