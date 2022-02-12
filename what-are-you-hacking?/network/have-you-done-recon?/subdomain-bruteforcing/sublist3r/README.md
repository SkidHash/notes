# sublist3r
## Install
```
sudo apt install sublist3r
```
## Examples
### Search for domains
```
sublist3r -d site.com
```
#### Successful Output
```
┌──(kali㉿kali)-[~]
└─$ sublist3r -d site.com       

                 ____        _     _ _     _   _____                         
                / ___| _   _| |__ | (_)___| |_|___ / _ __                    
                \___ \| | | | '_ \| | / __| __| |_ \| '__|                   
                 ___) | |_| | |_) | | \__ \ |_ ___) | |                      
                |____/ \__,_|_.__/|_|_|___/\__|____/|_|                      
                                                                             
                # Coded By Ahmed Aboul-Ela - @aboul3la                       
                                                                             
[-] Enumerating subdomains now for site.com                                 
[-] Searching now in Baidu..
[-] Searching now in Yahoo..
[-] Searching now in Google..
[-] Searching now in Bing..
[-] Searching now in Ask..
[-] Searching now in Netcraft..
[-] Searching now in DNSdumpster..
[-] Searching now in Virustotal..
[-] Searching now in ThreatCrowd..
[-] Searching now in SSL Certificates..
[-] Searching now in PassiveDNS..
[!] Error: Virustotal probably now is blocking our requests
[-] Total Unique Subdomains Found: 358
www.site.com
3.site.com
akamai-apigateway-automation.site.com
akamai-apigateway-bender.site.com
akamai-apigateway-captiveunderwriting.site.com
akamai-apigateway-crawford-prd.site.com
akamai-apigateway-crawford-stg.site.com
akamai-apigateway-deliveryopsapi.site.com
akamai-apigateway-deliveryopsapi1.site.com
akamai-apigateway-dev-warptmsapiserver.site.com
akamai-apigateway-einvoicing.site.com
akamai-apigateway-finplat-prd.site.com
akamai-apigateway-finplateng.site.com
akamai-apigateway-finplateng-routeone.site.com
akamai-apigateway-fta.site.com
akamai-apigateway-inventorytxnextapi.site.com
akamai-apigateway-logisticsratesapi.site.com
akamai-apigateway-materials.site.com
akamai-apigateway-mfs-supplier.site.com
akamai-apigateway-ops-warp3pl.site.com
akamai-apigateway-payment.site.com
akamai-apigateway-prd-global-deliveryopsapi.site.com
akamai-apigateway-procuretopayapi.site.com
akamai-apigateway-profileapi.site.com
akamai-apigateway-qa-captiveunderwriting.site.com
akamai-apigateway-scraprecycle.site.com
akamai-apigateway-shipmentplanningapi.site.com
akamai-apigateway-stg-bender.site.com
akamai-apigateway-stg-captiveunderwriting.site.com
akamai-apigateway-stg-deliveryopsapi.site.com
akamai-apigateway-stg-deliveryopsapi1.site.com
akamai-apigateway-stg-finplateng-defi.site.com
akamai-apigateway-stg-finplateng-routeone.site.com
akamai-apigateway-stg-fta.site.com
akamai-apigateway-stg-ops-warp3pl.site.com
akamai-apigateway-stg-packaging2.site.com
akamai-apigateway-stg-procuretopayapi.site.com
akamai-apigateway-stg-sandbox-automation.site.com
akamai-apigateway-stg-shipmentplanningapi.site.com
akamai-apigateway-stg-teslarpsapi.site.com
akamai-apigateway-stg-translationpipeline.site.com
akamai-apigateway-stg-vendorpartsapi.site.com
akamai-apigateway-stg-warp3pl.site.com
akamai-apigateway-stg-warpdashboardapi.site.com
akamai-apigateway-stg-warpedi.site.com
akamai-apigateway-stg-warptmsapiserver.site.com
akamai-apigateway-stg-warptqpapi.site.com
akamai-apigateway-stg2-global-deliveryopsapi.site.com
akamai-apigateway-translationpipeline.site.com
akamai-apigateway-uat-materials.site.com
akamai-apigateway-warp3pl.site.com
akamai-apigateway-warpcxml.site.com
akamai-apigateway-warpdashboardapi.site.com
akamai-apigateway-warpedi.site.com
akamai-apigateway-warptmsapiserver.site.com
akamai-apigateway-warptmsapiserver-upgrade.site.com
akamai-apigateway-warptqpapi.site.com
apac-sso.site.com
apacvpn.site.com
apacvpn1.site.com
api-account-master.site.com
api-firebolt.site.com
api-firebolt-dev.site.com
api-toolbox.site.com
sentry.app.site.com
appplayer.site.com
apps.site.com
aurora-ordering-ext-qa.site.com
aurora-ordering-ext-stg.site.com
auth.site.com
auth-global.site.com
auth-global-stage.site.com
autodiscover.site.com
awsbtest.site.com
bctpay.site.com
bender-auth.site.com
beta-partners.site.com
billing.site.com
blog.site.com
bolt.site.com
business-ui-ownership.site.com
ca.site.com
cdn-design.site.com
checkout-ui-assets.site.com
cicerone.site.com
ciscoguest.site.com
cld-ec.site.com
cloudprotect.site.com
cn.site.com
cnvpn.site.com
cnvpn1.site.com
comparison.site.com
manager.courses.site.com
sandbox-manager.courses.site.com
sandbox-studio.courses.site.com
www.sandbox-studio.courses.site.com
studio.courses.site.com
crpt.site.com
cryptopay.site.com
cryptopay2.site.com
cryptopay3.site.com
darkfield.site.com
dataviz.site.com
de.site.com
dev.site.com
digitalassets.site.com
digitalassets-energy.site.com
digitalassets-learning.site.com
digitalassets-shop.site.com
eaa-setup.site.com
edgedns.site.com
edr.site.com
einvoicing.site.com
email.site.com
click.email.site.com
image.email.site.com
mta.email.site.com
mta2.email.site.com
pages.email.site.com
view.email.site.com
email1.site.com
click.emails.site.com
image.emails.site.com
mta.emails.site.com
mta2.emails.site.com
mta3.emails.site.com
mta4.emails.site.com
mta5.emails.site.com
view.emails.site.com
employee-teslatequila.site.com
employeefeedback.site.com
energy.site.com
gridlogic.energy.site.com
www.gridlogic.energy.site.com
gridlogic-eng.energy.site.com
powerhub.energy.site.com
www.powerhub.energy.site.com
autobidder.powerhub.energy.site.com
autobidder-eng.powerhub.energy.site.com
autobidder-preprd.powerhub.energy.site.com
gridlogic.powerhub.energy.site.com
gridlogic-eng.powerhub.energy.site.com
energydesk.site.com
energysupport.site.com
engage.site.com
envoy-finplat-stg.site.com
envoy-partnerleadsharing.site.com
envoy-partnertasks.site.com
epc.site.com
epcapi.site.com
errlog.site.com
eua-origin.site.com
eumirror.site.com
events.site.com
external-3pl-stg.site.com
factory-berlin.site.com
feedback.site.com
financial-gw.site.com
financial-gw-stg.site.com
finops.site.com
forums.site.com
gf-modeling-mpp.site.com
github.site.com
github-it.site.com
assets.github-it.site.com
avatars.github-it.site.com
codeload.github-it.site.com
docker.github-it.site.com
gist.github-it.site.com
maven.github-it.site.com
media.github-it.site.com
npm.github-it.site.com
nuget.github-it.site.com
pages.github-it.site.com
raw.github-it.site.com
render.github-it.site.com
reply.github-it.site.com
rubygems.github-it.site.com
uploads.github-it.site.com
grid.site.com
image-emails.site.com
imap.site.com
inside.site.com
installations-ext-api.site.com
inventory-assets.site.com
invest.site.com
ir.site.com
itanswers.site.com
kronos.site.com
integration.kronos.site.com
mobile.kronos.site.com
wdm.kronos.site.com
wim.kronos.site.com
kronos-dev.site.com
kronosdb.site.com
link.site.com
o1.ptr2410.link.site.com
links.site.com
lionpayshare.site.com
lionpaytest.site.com
lionshare.site.com
livestream.site.com
livestreamapi.site.com
livestreamapi-test.site.com
location-services-prd.site.com
logcollection.site.com
lyncdiscover.site.com
marketing.site.com
meet.site.com
mfa.site.com
mfa-dev.site.com
mfa-reset.site.com
mfamobile-dev.site.com
mfauser-dev.site.com
mfg.site.com
mfs-supplier.site.com
mfs-supplier-uat.site.com
mirror.site.com
mobile.site.com
model3.site.com
monitoring.site.com
mrsproxy06.site.com
my.site.com
myapps.site.com
na-1-sso.site.com
na-2-sso.site.com
na-sso.site.com
naa-origin.site.com
nas-origin.site.com
new.site.com
new-dev.site.com
nv.site.com
ny.site.com
onboard.site.com
oneteam.site.com
origin-apps.site.com
origin-auth.site.com
origin-bolt.site.com
origin-courses.site.com
origin-edr.site.com
origin-einvoicing.site.com
origin-financialgateway-stg.site.com
origin-grid.site.com
origin-inside.site.com
origin-itanswers.site.com
origin-mfa.site.com
origin-mobile.site.com
origin-ownership.site.com
origin-pilotbpay.site.com
origin-profile.site.com
origin-ranger-api.site.com
origin-referral-app.site.com
origin-slingsdlc.site.com
origin-tcc-gw.site.com
origin-tcc-gw-stg.site.com
origin-toolbox-beta.site.com
origin-warp.site.com
origin-warp-stg.site.com
origin-www.site.com
origin-www-auth.site.com
origin-wwwcdn.site.com
os.site.com
ownership.site.com
partnerleadsharing.site.com
partners.site.com
pilot-bpay.site.com
pm-bounces.site.com
pop.site.com
powerwall.site.com
productinfo.site.com
profile.site.com
o3.ptr1444.site.com
o4.ptr1867.site.com
o2.ptr556.site.com
o7.ptr6980.site.com
o5.ptr8466.site.com
o6.ptr9437.site.com
qa.site.com
referral.site.com
referral-app.site.com
repair.site.com
resources.site.com
rumipv6.site.com
studio.sandbox-courses.site.com
sca.site.com
schedule.site.com
secure-static-assets.site.com
secureguest.site.com
secureguestcn.site.com
server.site.com
service.site.com
serviceapi.site.com
serviceapi-stg.site.com
serviceapp.site.com
share.site.com
shop.site.com
simpleorigin.site.com
sip.site.com
sjc04d1rsaap02.site.com
sling.site.com
smarttax.site.com
smtp.site.com
solarbonds.site.com
sso.site.com
sso-dec.site.com
sso-dev.site.com
sso-sig.site.com
sspr.site.com
stage.site.com
stage-traffic-flow-test.site.com
static.site.com
static-assets.site.com
static-assets-pay.site.com
static-assets-teslaaccount.site.com
static-event-dev.site.com
static-map.site.com
staticpay-origin-wwwcdn.site.com
stg-uc-twilio-bpm-webhook.site.com
tcc-gw.site.com
teamchat.site.com
teslacdpna0.site.com
teslaquila.site.com
www.teslaquila.site.com
teslatequila.site.com
www.teslatequila.site.com
three.site.com
toolbox.site.com
www.toolbox.site.com
toolbox-beta.site.com
tradein.site.com
tradepartnertickets.site.com
trt.site.com
tweventhook.site.com
tx.site.com
ug.site.com
www.ug.site.com
url1894.site.com
url2547.site.com
url4104.site.com
url5196.site.com
url7051.site.com
vmanage-alerts.site.com
vpn1.site.com
www.vpn1.site.com
vpn2.site.com
warehouse.site.com
warpbilling.site.com
webmail.site.com
www-dev.site.com
www-static-stage.site.com
www-stg2.site.com
www-test.site.com
www-uat.site.com
www-uat2.site.com
www45.site.com
xapps.site.com
xmail.site.com
zta-setup.site.com
                                                                             
┌──(kali㉿kali)-[~]
└─$ 
```

#### Failed output
```
┌──(kali㉿kali)-[~]
└─$ sublist3r -d oanoaoiafoianf.asodnaonasio

                 ____        _     _ _     _   _____
                / ___| _   _| |__ | (_)___| |_|___ / _ __
                \___ \| | | | '_ \| | / __| __| |_ \| '__|
                 ___) | |_| | |_) | | \__ \ |_ ___) | |
                |____/ \__,_|_.__/|_|_|___/\__|____/|_|

                # Coded By Ahmed Aboul-Ela - @aboul3la                                                                     
                                                                                                                           
[-] Enumerating subdomains now for oanoaoiafoianf.asodnaonasio                                                             
[-] Searching now in Baidu..
[-] Searching now in Yahoo..
[-] Searching now in Google..
[-] Searching now in Bing..
[-] Searching now in Ask..
[-] Searching now in Netcraft..
[-] Searching now in DNSdumpster..
[-] Searching now in Virustotal..
[-] Searching now in ThreatCrowd..
[-] Searching now in SSL Certificates..
[-] Searching now in PassiveDNS..
[!] Error: Virustotal probably now is blocking our requests
                                                                                                                           
┌──(kali㉿kali)-[~]
└─$
```

### searching with 100 additional threads
```
sublist3r -d site.com -t 100
```
#### Successful output
See
#### Bad output