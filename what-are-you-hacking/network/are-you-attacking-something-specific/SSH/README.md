# SSH
## Default port
22
## Examples
### Logging in with ssh (will be prompted for password)
```
ssh $USERNAME@$IP
```
###  Logging in with user's private key for authentication
```
ssh $USERNAME@$IP -i local_id_rsa_file_for_username.pem
```