# Quality of Life Improvements in Kali
These are totally optional 
## Pimp My Kali
### URL
https://github.com/Dewalt-arch/pimpmykali
### What does it do?
Installs a ton of useful tools that help resolve issues in later distros as well as good tools for certifications.  This individual is at this time associated with TheCyberMentor so a lot of additional resources are tailored around the resources and content they recommend/use (not that thats bad you just might disagree or not use some things)
### install
```
git clone https://github.com/Dewalt-arch/pimpmykali.git
cd pimpmykali
sudo ./pimpmykali.sh

```
#### Successful Output
```
           .__                               __           .__  .__ 
    ______ |__| _____ ______   _____ ___.__.|  | _______  |  | |__|
    \____ \|  |/     \____  \ /     \|  |  ||  |/ /\__  \ |  | |  |
    |  |_> >  |  Y Y  \  |_> >  Y Y  \___  ||    <  / __ \|  |_|  |
    |   __/|__|__|_|  /   __/|__|_|  / ____||__|_ \(____  /____/__|
    |__|            \/|__|         \/\/ Powered  \/  By \/  Dewalt

    Select an option from menu:                           Rev:1.4.3

 Key  Menu Option:             Description:
 ---  ------------             ------------
  1 - Fix Missing              (pip pip3 golang gedit nmapfix build-essential)
  2 - Fix /etc/samba/smb.conf  (adds the 2 missing lines)
  3 - Fix Golang               (installs golang, adds GOPATH= to .zshrc and .bashrc)
  4 - Fix Grub                 (adds mitigations=off)
  5 - Fix Impacket             (installs impacket)
  6 - Enable Root Login        (installs kali-root-login)
  7 - Install Atom             (installs atom)
  8 - Fix nmap scripts         (clamav-exec.nse and http-shellshock.nse)
  9 - Pimpmyupgrade            (apt upgrade with vbox/vmware detection)
                               (sources.list, linux-headers, vm-video)
  0 - Fix ONLY 1 thru 8        (runs only 1 thru 8) 

  N - NEW VM SETUP - Run this option if this is the first time running pimpmykali

  = - Pimpmykali-Mirrors       (find fastest kali mirror. use the equals symbol = )
  T - Reconfigure Timezone      current timezone  : America/Chicago
  K - Reconfigure Keyboard      current keyb/lang : us

 Key  Stand alone functions:   Description:
 ---  ----------------------   ------------
  B - BlindPentesters          (The Essentials tools & utilies collection)
  C - Missing Google-Chrome    (install google-chrome only)
  D - Downgrade Metasploit     (Downgrade from MSF6 to MSF5)
  F - Broken XFCE Icons fix    (stand-alone function: only applies broken xfce fix)
  G - Fix Gedit Conn Refused   (fixes gedit as root connection refused)
  H - Fix httprobe missing     (fixes httprobe missing only)
  L - Install Sublime Editor   (install the sublime text editor)
  M - Mayors MPP Course Setup  (adds requirments for Mayors MPP Course)
  P - PPA Course Setup         (adds requirments for Graham Helton - PPA Course)
  A - MAPT Course Setup        (adds requirments for MAPT Course)
  S - Fix Spike                (remove spike and install spike v2.9)
  W - Gowitness Precompiled    (download and install gowitness)
  V - Install MS-Vscode        (install microsoft vscode only)
  ! - Nuke Impacket            (Type the ! character for this menu item)

  Press key for menu item selection or press X to exit:

  //  There is a lot of output here
  //  N is recommended for a brand new Kali VM


           .__                               __           .__  .__ 
    ______ |__| _____ ______   _____ ___.__.|  | _______  |  | |__|
    \____ \|  |/     \____  \ /     \|  |  ||  |/ /\__  \ |  | |  |
    |  |_> >  |  Y Y  \  |_> >  Y Y  \___  ||    <  / __ \|  |_|  |
    |   __/|__|__|_|  /   __/|__|_|  / ____||__|_ \(____  /____/__|
    |__|            \/|__|         \/\/ Powered  \/  By \/  Dewalt


    All Done! Happy Hacking! 

                                                                                                                                               
┌──(kali㉿kali)-[~/pimpmykali]
└─$
```