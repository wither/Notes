# LazyAdmin

![](https://tryhackme-images.s3.amazonaws.com/room-icons/efbb70493ba66dfbac4302c02ad8facf.jpeg)

---

## nmap

![](images/nmap.png)  

## website

> The IP loads default Apache2 `index.html`

![](images/default.png)  

## ffuf

> find the `/content/` folder

![](images/ffuf.png) 

> `/content/` loads this page

![](images/sweetrice.png)  

> More folders in content, one of them being a login portal called `/as/`.

![](images/as.png)  

![](images/loginportal.png)  

> Another being `/inc/`, in which the `MySQL` backup file can be downloaded, revealing admin credentials

![](images/inc.png)  

![](images/creds.png)  

> Crack the password

![](images/cracked.png)  

> Use this `arbitrary file upload` exploit to upload a `php` file

![](images/upload.png)  

![](images/hacked.png) 

> Change `echo "hacked"` to a reverse shell, upload and open a listener to get the user `www-data`.

![](images/user.png)  

> `www-data` can run `perl` and a backup file called `backup.spl` as sudo

![](images/sudo.png)  

## User flag

![](images/userflag.png)  

## PrivEsc

> `backup.pl` runs `/etc/copy.sh`

![](images/backup.png)  

> Change `copy.sh` to a reverse shell and run `backup.pl` as sudo to get a reverse shell.

![](images/copy.png)  

## Root

![](images/root.png)  

## Root flag

![](images/rootflag.png)  

