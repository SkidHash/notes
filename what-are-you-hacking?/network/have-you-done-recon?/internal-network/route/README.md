# route
## Explanation
### man pages
Route is a utility used to manually manipulate the network routing tables.  It normally is not needed, as a system routing table management daemon such as routed(8), should tend to this task.

The route utility supports a limited number of general options, but a rich command language, enabling the user to specify any arbitrary request that could be delivered via the programmatic interface discussed in route(4)

### flags
#### -d
debug mode.  Do not modify the routing table
#### -n
Bypass attempts to print host and network names symbolically when reporting actions
#### -t
run in test mode
#### -v
verbose mode

## Examples
### see basic route info
```
route
```
##### Successful output
```
┌──(kali㉿kali)-[~]
└─$ route               
Kernel IP routing table
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
default         172.16.210.2    0.0.0.0         UG    100    0        0 eth0
172.16.210.0    0.0.0.0         255.255.255.0   U     100    0        0 eth0

```