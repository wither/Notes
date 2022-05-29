# LazyAdmin

![](https://tryhackme.com/img/banners/default_tryhackme.png)

---

## nmap

![](images/nmap.png)  

## website

> going to the IP loads default apache2 index.html

![](images/default.png)  

## ffuf

> find content folder

![](images/ffuf.png) 

> /content/ loads this page

![](images/sweetrice.png)  

> more folders in content, one of them being a login portal (/as/)

![](images/as.png)  

![](images/loginportal.png)  

> another being /inc/, in which the mysql backup file can be downloaded, revealing admin credentials

![](images/inc.png)  

![](images/creds.png)  

> crack the password

![](images/cracked.png)  

> use this arbitrary file upload exploit to upload a php file

![](images/upload.png)  

![](images/hacked.png) 

> change echo "hacked" to a reverse shell, upload and listen for it to get user

![](images/user.png)  

> user can run perl and a backup file as sudo

![](images/sudo.png)  

## User flag

![](images/userflag.png)  

## PrivEsc

> backup.pl runs /etc/copy.sh

![](images/backup.png)  

> change copy.sh to a reverse shell and run backup.pl as sudo to get a reverse shell

![](images/copy.png)  

## Root

![](images/root.png)  

## Root flag

![](images/rootflag.png)  

