# tech-supp0rt-1

![](https://tryhackme-images.s3.amazonaws.com/room-icons/4128774917fae71184e79acab2007e93.png)

---

## nmap

![](images/nmap.png)  

## ffuf

> There is a directory `/test/`

![](images/test.png)  

## smb

> Enumerate `SMB` shares using `nmap`'s `smb-enum-shares` script.

![](images/shares.png)  

> Login to the `/websvr` share and download the `enter.txt` file

![](images/txt.png)  

> `enter.txt` has admin credentials 

![](images/creds.png)  

## cracking

> Use `cyberchef magic recipe` to crack the password

![](images/crack.png)  

## exploit

> Use this exploit to get `RCE`

![](images/exploit.png)  

## shell

> Use the `RCE` to download and run a reverse shell

![](images/shell.png)    

## PrivEsc

> `wp-config` file in `/wordpress/` contains credentials

![](images/wpcreds.png)  

> `/etc/passwd` shows that `scamsite` is the other user

![](images/scamsite.png)  

## User

> Use the `wordpress` password to `SSH` into the machine as `scamsite`

![](images/userssh.png)  

## PrivEsc to root

> `iconv` can be ran as sudo without password

![](images/sudo.png)  

## Root flag

> exploit `iconv` to read the root flag
 
![](images/rootflag.png)  
