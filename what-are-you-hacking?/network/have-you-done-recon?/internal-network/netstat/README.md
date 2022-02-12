# netstat
## Examples
### see open ports with process running on port
```
netstat -ano
```
#### Successful Output
```
┌──(kali㉿kali)-[~]
└─$ netstat -ano 
Active Internet connections (servers and established)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       Timer
tcp        0      0 172.16.210.128:48776    104.21.22.45:443        ESTABLISHED off (0.00/0/0)
tcp        0      0 172.16.210.128:43524    3.216.211.240:443       ESTABLISHED off (0.00/0/0)
tcp        0      0 172.16.210.128:37940    35.244.181.201:443      TIME_WAIT   timewait (31.64/0/0)
tcp        0      0 172.16.210.128:48738    99.86.74.64:443         ESTABLISHED off (0.00/0/0)
tcp        0      0 172.16.210.128:37880    140.82.112.25:443       ESTABLISHED keepalive (344.86/0/0)
tcp        0      0 172.16.210.128:32938    34.98.75.36:443         ESTABLISHED off (0.00/0/0)
tcp        0      0 172.16.210.128:42184    172.67.152.52:443       TIME_WAIT   timewait (34.66/0/0)
tcp        0      0 172.16.210.128:37516    13.226.184.92:443       ESTABLISHED keepalive (2.22/0/0)
tcp        0      0 172.16.210.128:58668    140.82.113.3:443        ESTABLISHED off (0.00/0/0)
tcp        0      0 172.16.210.128:46436    65.8.228.81:443         TIME_WAIT   timewait (32.60/0/0)
tcp        0      0 172.16.210.128:55874    52.40.161.235:443       ESTABLISHED keepalive (340.30/0/0)
udp        0      0 172.16.210.128:68       172.16.210.254:67       ESTABLISHED off (0.00/0/0)
raw6       0      0 :::58                   :::*                    7           off (0.00/0/0)
Active UNIX domain sockets (servers and established)
Proto RefCnt Flags       Type       State         I-Node   Path
unix  2      [ ACC ]     STREAM     LISTENING     14643    /run/systemd/userdb/io.systemd.DynamicUser
unix  2      [ ACC ]     STREAM     LISTENING     14644    /run/systemd/io.system.ManagedOOM
unix  2      [ ]         DGRAM                    14653    /run/systemd/journal/syslog
unix  2      [ ACC ]     STREAM     LISTENING     14655    /run/systemd/fsck.progress
unix  12     [ ]         DGRAM                    14659    /run/systemd/journal/dev-log
unix  6      [ ]         DGRAM                    14661    /run/systemd/journal/socket
unix  2      [ ACC ]     STREAM     LISTENING     14663    /run/systemd/journal/stdout


//  There is a lot more output that is omitted
```