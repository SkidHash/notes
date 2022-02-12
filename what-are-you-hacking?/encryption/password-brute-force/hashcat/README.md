# hashcat
## Examples
### Brute Forcing a Hash Via Wordlist
```
hashcat -a 0 -m $MODE file_with_hash.hash passwd_wordlist.txt
```
#### Flags
##### -m
This value is obtained from looking at the wiki examples
https://hashcat.net/wiki/doku.php?id=example_hashes
##### -a
The attack mode.:
1. 0 is wordlist
1. 1 is combination
1. 3 is brute force
1. 6 is hybrid wordlist + mask
1. 7 is hybrid mask + wordlist
1. 9 is association

#### Examples
##### Success
```
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ hashcat -a 0 -m 18200 asrep_hash.hash pass_list.txt
hashcat (v6.2.5) starting

OpenCL API (OpenCL 2.0 pocl 1.8  Linux, None+Asserts, RELOC, LLVM 11.1.0, SLEEF, POCL_DEBUG) - Platform #1 [The pocl project]
=============================================================================================================================
* Device #1: pthread-0x000, 3663/7390 MB (1024 MB allocatable), 4MCU

Minimum password length supported by kernel: 0
Maximum password length supported by kernel: 256

Hashes: 1 digests; 1 unique digests, 1 unique salts
Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
Rules: 1

Optimizers applied:
* Zero-Byte
* Not-Iterated
* Single-Hash
* Single-Salt

ATTENTION! Pure (unoptimized) backend kernels selected.
Pure kernels can crack longer passwords, but drastically reduce performance.
If you want to switch to optimized kernels, append -O to your commandline.
See the above message to find out about the exact limits.

Watchdog: Temperature abort trigger set to 90c

Host memory required for this attack: 1 MB

Dictionary cache built:
* Filename..: pass_list.txt
* Passwords.: 70189
* Bytes.....: 569237
* Keyspace..: 70189
* Runtime...: 0 secs

$krb5asrep$23$svc-admin@spookysec.local@THM-AD:5075e0a73adb4ff21b0dc6a6a000d115$92f853852980746d406fc4eb36ec684f61d22e1e362637ceb8b08b8b13bd02006ddbb004dfa6a0221cf5aa72e3e278548d198cd5a64e4c80c42a9b5b22255f2e3bef7aaa84db26c1b7795c4451514b96527ccc8fdf22e01315fe66431d0b6e6676d27f7da7a0c8dd6cf1d6c0b723e26f90ca9d260775a5bf593a8b67d85b63f6ccdcb3491fcc408e0970c063dd144f30e2981aec530007c7fdb41ff088b7dbb49cc2e712dc32805706a1d0d9005c1097ad814838fd8105be62c6a1a31275768acde7c1a04dcaea969f7bc7fb7fa33e122e0865bb0c7264db31cff7198b00425eda6b175b65289ec207:management2005
                                                          
Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 18200 (Kerberos 5, etype 23, AS-REP)
Hash.Target......: $krb5asrep$23$svc-admin@spookysec.local@THM-AD:5075...9ec207
Time.Started.....: Sat Feb 12 11:10:19 2022 (0 secs)
Time.Estimated...: Sat Feb 12 11:10:19 2022 (0 secs)
Kernel.Feature...: Pure Kernel
Guess.Base.......: File (pass_list.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:   272.1 kH/s (0.79ms) @ Accel:512 Loops:1 Thr:1 Vec:4
Recovered........: 1/1 (100.00%) Digests
Progress.........: 8192/70189 (11.67%)
Rejected.........: 0/8192 (0.00%)
Restore.Point....: 6144/70189 (8.75%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#1....: horoscope -> whitey
Hardware.Mon.#1..: Util: 25%

Started: Sat Feb 12 11:10:18 2022
Stopped: Sat Feb 12 11:10:21 2022
                                                                                                                           
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ hashcat -a 0 -m 18200 asrep_hash.hash pass_list.txt --show             
$krb5asrep$23$svc-admin@spookysec.local@THM-AD:5075e0a73adb4ff21b0dc6a6a000d115$92f853852980746d406fc4eb36ec684f61d22e1e362637ceb8b08b8b13bd02006ddbb004dfa6a0221cf5aa72e3e278548d198cd5a64e4c80c42a9b5b22255f2e3bef7aaa84db26c1b7795c4451514b96527ccc8fdf22e01315fe66431d0b6e6676d27f7da7a0c8dd6cf1d6c0b723e26f90ca9d260775a5bf593a8b67d85b63f6ccdcb3491fcc408e0970c063dd144f30e2981aec530007c7fdb41ff088b7dbb49cc2e712dc32805706a1d0d9005c1097ad814838fd8105be62c6a1a31275768acde7c1a04dcaea969f7bc7fb7fa33e122e0865bb0c7264db31cff7198b00425eda6b175b65289ec207:management2005
                                                                                                                           
┌──(kali㉿kali)-[~/Documents/attacktive-directory]
└─$ 
```

In the second run you can see the cracked password is management2005