# tomghost

![](https://i.imgur.com/j83SrGu.png)

## nmap

![](images/nmap.png)

## ssh

> Exploit tomcat using the ghostcat vulnerability (metasploit) and get the user 'skyfuck' ssh login:
(skyfuck : 8730281lkjlkjdqlksalks)

![](images/exploitandssh.png)

## scp

scp the files from /home/skyfuck onto my machine
![](images/scp.png)

## gpgjohn

Crack the asc file to get hashes that we can later pass into johntheripper
![](images/gpgjohn.png)

## john

crack the hashes to get the passphrase
![](images/john.png)

## gpg

import the .asc file to decrypt the credentials to get a new user (merlin : asuyusdoiuqoilkda312j31k2j123j1g23g12k3g12kj3gk12jg3k12j3kj123j)
![](images/merlin.png)

## User Flag

![](images/userflag.png)

## PrivEsc

sudo -l to show sudo binaries (zip)
exploit it to escalate privelages (https://gtfobins.github.io/gtfobins/zip/)
![](images/privesc.png)

## Root Flag

get root flag
![](images/rootflag.png)
