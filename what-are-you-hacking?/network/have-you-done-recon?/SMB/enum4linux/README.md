# enum4linux
## Examples
### Getting shares on a system
```
$> enum4linux -S $IP
```
#### Flags
##### S
retrieves the sharelist for the system
### Getting all information on a system
```
$> enum4linux -a $IP
```
#### Flags
##### a
performs all simple enumerations (-U -S -G -P -r -o -n -i)

This flag is enabled by default if there are no args
