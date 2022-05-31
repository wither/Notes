# overpass

![](https://tryhackme-images.s3.amazonaws.com/room-icons/2048656e072dd7caffe455ae2d44b65f.png)

---

## Nmap

![](images/nmap.png)  

## Ffuf

> `/admin/` is a login page

![](images/ffuf.png)  

> it uses `login.js` that shows "Incorrect Credentials" if there is no cookie

![](images/cookie.png)  

> so by setting a cookie, `login.js` no longer displays `"Incorrect Credentials"` and instead allows access to `James`'s SSH key

![](images/sshkey.png) 

## John

> Save the key and pass it to `ssh2john`

![](images/ssh2john.png)  

> Pass the hash to `john` and get a password

![](images/sshpass.png) 

## User flag

> Enter the passphrase and login

![](images/login.png)  

## PrivEsc

> `todo.txt` tells `Paradox` to get an automatic build script working, which they seem to have done as shown in `/etc/crontab`. Theres a cronjob to get and run `buildscript.sh` from `overpass.thm`, which must be a reference in `/etc/hosts`

![](images/crontab.png)  

> `/etc/hosts` is `writable`, change the IP assigned to `overpass.thm`

![](images/hosts.png)  

## Root

> Write a reverse shell script called `buildscript.sh` in a folder called `/downloads/src` and start a http server there, the `cronjob` will `wget` and `run it` to give a root shell.
 
![](images/root.png)  

## Root flag

![](images/rootflag.png)  