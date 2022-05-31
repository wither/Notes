# ide

![](https://tryhackme-images.s3.amazonaws.com/room-icons/3ce8e9c4d1da5eefef690e11f75798c7.png)

---

## Nmap

![](images/nmap.png)  

## Website

> There is a `codiad` login portal on port `62337`

![](images/login.png)  

## FTP

> Login to FTP with `anonymous:anonymous` and `get .../-`. `drac` reset the pasword for `john`.

![](images/-.png)  

## Login

> Login with johns credentials

![](images/passreset.png)  


## Exploit

> Use this RCE exploit in codiad to get a reverse shell

![](images/shell.png)  

## PrivEsc

> drac is the other user

![](images/drac.png)  

> drac's password is in their `.bash_history`

![](images/retracted.png)  

## User flag

> SSH into the machine as the `drac` user using his password

![](images/ssh.png)  

## PrivEsc to root

> drac can `restart` FTP as sudo, essentially running the config file

![](images/config.png)

> Change `ExecStart` variable to a reverse shell so that it execute upon FTP starting back up.

![](images/editservice.png)  

> Restart system daemons and run the sudo command

![](images/servicerestart.png)  

## Root

> Open a listener and wait for root

![](images/root.png)  

## Root flag

![](images/rootflag.png)  



