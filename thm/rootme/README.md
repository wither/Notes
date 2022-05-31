# RootMe

![](https://tryhackme-images.s3.amazonaws.com/room-icons/11d59cb34397e986062eb515f4d32421.png)

---

## nmap

![](images/nmap.png)  

## ffuf

> Found two hidden directories, `/panel/` and `/uploads/`

![](images/ffuf.png)  

## upload

> `/panel/` is a file upload interface

![](images/upload.png)  

> PHP uploads `arent` allowed

![](images/nophp.png)  

> Rename the reverse shell file to `.php5` to bypass the filter

![](images/bypass.png)  

> Open a netcat listener and go to `/uploads/shell.php`5 to get a reverse shell

![](images/shell.png)  

## User flag

![](images/user.png)  

## PrivEsc

> Find `suid` binaries, `python` is exploitable

![](images/suid.png)  

## Root

> Exploit the fact that `python` has `SUID` permissions set to get root.

![](images/root.png)  

## Root flag

![](images/rootflag.png)  

