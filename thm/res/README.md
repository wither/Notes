# res

![](https://assets.tryhackme.com/room-banners/redis.png)

---

## nmap

![](images/nmap.png)

## redis-cli

connect using redis-cli
![](images/rediscli.png)

## rce

we have remote code execution
![](images/rce.png)
![](images/id.png)

## reverse shell

use netcat to get a reverse shell
![](images/shell.png)
![](images/webshell.png)

upgrade shell
![](images/upgrade.png)

## PrivEsc to Vianka

linenum suid binaries list xxd (https://gtfobins.github.io/gtfobins/xxd/)
![](images/linenum.png)

exploit xxd to read /etc/shadow and /etc/passwd and save both to files on my machine
![](images/vianka.png)  
![](images/unshadow.png)

crack the unshadow file with john
![](images/cracked.png)

## User Flag

![](images/userflag.png)

## PrivEsc to Root

use the same exploit to read sudoers file and copy it to a new file
![](images/sudoers.png)

add vianka to the new sudoers file and overwrite the original, then switch to root  
![](images/root.png)

## Root Flag

![](images/rootflag.png)
