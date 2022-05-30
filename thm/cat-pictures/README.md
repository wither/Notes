# cat-pictures

![](https://tryhackme-images.s3.amazonaws.com/room-icons/0d75a543c66201b4aa996172b6043eb5.jpeg)

---

## nmap

![](images/nmap.png)  

## ftp

> ftp is filtered, knocking these ports found on the forums only post opens it up and anonymous login is enabled. get note.txt

![](images/magicnumbers.png)  

![](images/ftpopen.png)  

> says to connect on port 4420 with a password

![](images/4420.png)  

## netcat

> using the password login using netcat and spawn a reverse shell

![](images/rs.png)  

## runme

> theres a file in catlover's home called runme that asks for a password

![](images/runme.png)  

> suspected password in the source

![](images/rebecca.png)  

> rebecca as a password generates an id_rsa

![](images/idrsa.png)  

## Fake root

> use the key to ssh as fake root

![](images/root.png) 

## Flag 1

![](images/flag1.png)  

## PrivEsc

> cat /etc/crontab wont work, .bash_history shows repetitive access to /opt/clean.sh and crontab

![](images/cron.png)  

## Root

> add a reverse shell onto clean.sh and wait for the cronjob to get a shell

![](images/rootrs.png)  

## Root flag

![](images/rootflag.png)  