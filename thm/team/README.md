# Team

![](https://tryhackme-images.s3.amazonaws.com/room-icons/e8171ef71802f0f254bd38ffb0beff4b.png)

## Rustscan

![](images/rustscan.png)  

## Robots

> name in robots.txt

![](images/dale.png)  

## Script

> /scripts/ reveals a script, at the bottom says the old one contained creds

![](images/script.png)  

> script.old is the old script

![](images/old.png)  

## FTP

> login with those credentials and download `workshare/New_site.txt`

![](images/newsite.png)  

## New Site

> dale says hes making a new PHP website on the dev. subdomain

![](images/dev.png)  

> new site has a placeholder page

![](images/placeholder.png)  

> change the URL to read a different file (LFI)

![](images/lfi.png)  

> /etc/ssh/sshd_config gives dale's id_rsa

![](images/daleidrsa.png)  

## User

> save the id_rsa and ssh as dale

![](images/sshdale.png)  

## User flag

![](images/userflag.png)  

## PrivEsc

> dale can run this script as gyles

![](images/sudol.png)  

> inject /bin/bash into the script as the date variable to get a shell as gyles

![](images/gylesuser.png)  

## PrivEsc to Root

> noticed /usr/local/bin in the PATH, theres a backup script in there that gyles can edit, add a reverse shell and open a listener

![](images/root.png)  

## Root flag

![](images/rootflag.png)  