# Nmap
## Purpose
General port scanner.  Great opening move for any type of network recon.

Recommended on individual targets.  Slower when scanning multiple targets/networks
## Examples
### All port verbose version scan on target
```
$> sudo nmap -sV -p- -vv $IP 
```
#### Flags
##### sV
Will try to determine versions of any software taking up a port

### Running Vuln Scripts on target (WARNING: DANGEROUS!!!)
```
$> sudo nmap --script=vuln $IP
```
#### Flags
##### script=vuln
Will run the Nmap Script Explorer, specifically the scripts under vuln.

Scripts are located at the following in kali:
`/usr/share/nmap/scripts`
