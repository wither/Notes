# cat-pictures

![](https://tryhackme-images.s3.amazonaws.com/room-icons/0d75a543c66201b4aa996172b6043eb5.jpeg)

---

## nmap

![](images/nmap.png)  

## ftp

> FTP is `filtered`, `knocking` the ports found on the forum opens it up. Login using `anonymous:anonymous` and download `note.txt`

![](images/magicnumbers.png)  

![](images/ftpopen.png)  

> `note.txt` says to connect on port 4420 with a password.

![](images/4420.png)  

## netcat

> Using the password, login using `netcat` and spawn a reverse shell.

![](images/rs.png)  

## runme

> There's a file in `catlover`'s home called `runme` that asks for a password.

![](images/runme.png)  

> The password is hard-coded into the source.

![](images/rebecca.png)  

> The password generates an rsa SSH key `id_rsa`

![](images/idrsa.png)  

## Fake root

> Use the key to SSH as fake root.

![](images/root.png) 

## Flag 1

![](images/flag1.png)  

## PrivEsc

> `cat /etc/crontab` wont work, `.bash_history` shows repetitive access to `/opt/clean.sh` and `/etc/crontab`

![](images/cron.png)  

## Root

> Append a reverse shell onto `clean.sh` and wait for the cronjob to get a shell.

![](images/rootrs.png)  

## Root flag

![](images/rootflag.png)  