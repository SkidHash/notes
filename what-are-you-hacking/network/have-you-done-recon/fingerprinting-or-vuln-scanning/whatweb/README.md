# whatweb
Web scanning and fingerprinting
## Examples
### Basic verbose stealth scan
```
whatweb site.com -a=1 -v
```
#### Successful Output
```
┌──(kali㉿kali)-[~]
└─$ whatweb https://site.com
https://site.com [301 Moved Permanently] Akamai-Global-Host, Country[EUROPEAN UNION][EU], HTTPServer[AkamaiGHost], IP[2.20.92.122], RedirectLocation[https://www.site.com/], Strict-Transport-Security[max-age=15768000], UncommonHeaders[permissions-policy]
https://www.site.com/ [200 OK] Access-Control-Allow-Methods[GET,POST,OPTIONS], Content-Language[en], Country[UNITED STATES][US], Drupal, Frame, HTML5, IP[173.222.252.81], MetaGenerator[Drupal 9 (https://www.drupal.org)], Open-Graph-Protocol[website], PHP[7.4.16], PoweredBy[Site], Script[application/json,text/javascript], Strict-Transport-Security[max-age=15768000], Title[Electric Cars, Solar &amp; Clean Energy | Site], UncommonHeaders[x-drupal-dynamic-cache,x-generator,x-drupal-cache,x-tzla-edge-hostname-vcl,x-tzla-edge-backend-fetch-if-stale,x-tzla-edge-was-304,x-tzla-edge-age,x-tzla-edge-grace,x-tzla-edge-backend-retry,x-tzla-edge-backend-conn-time,x-tzla-edge-backend-ttfb,x-tzla-edge-backend-reason,x-tzla-edge-backend-status,x-varnish,x-content-type-options,x-tzla-edge-cache-hit,x-tzla-edge-ttl,x-tzla-edge-grace-backend-unhealthy,x-tzla-edge-backend-stream,x-tzla-edge-client-restarts,x-tzla-edge-client-req-ttl,x-tzla-edge-server,x-tzla-edge-cache-hits,access-control-allow-origin,access-control-allow-methods,permissions-policy], Varnish, X-Frame-Options[SAMEORIGIN], X-Powered-By[PHP/7.4.16], X-UA-Compatible[IE=edge]
                                                                                                                           
┌──(kali㉿kali)-[~]
└─$
```
#### Failed Output
```
┌──(kali㉿kali)-[~]
└─$ whatweb asoiaoinionfionosdf.asindaisndoiansio                                                                    130 ⨯
ERROR Opening: http://asoiaoinionfionosdf.asindaisndoiansio - no address for asoiaoinionfionosdf.asindaisndoiansio
                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ 
```

### Aggressive scan (will try to ID web plugins)
```
```
#### Successful Output
#### Failed Output

### Scan local network and suppress errors (e.g. suppress hosts not up)
```
whatweb --no-errors 192.168.0.0/24
```
#### Successful Output
```
```

#### Failed Output
```
```

### Scan local network for https websites
```
whatweb --no-errors --url-prefix https:// 192.168.0.0/24
```
#### Successful Output
Nothing because I dont have any https on my lan
#### Failed Output

