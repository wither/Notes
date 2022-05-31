# res

![](https://tryhackme-images.s3.amazonaws.com/room-icons/828d4be9917a0dc62fa09ac05265cd7b.png)

---

## nmap

![](images/nmap.png)

## redis-cli

> Connect using `redis-cli`

![](images/rediscli.png)

## RCE

> Make a new redis php db to perform `RCE`

![](images/rce.png)

![](images/id.png)

## reverse shell

> Use netcat and the `RCE` to get a reverse shell

![](images/shell.png)

![](images/webshell.png)

> Upgrade the shell using python

![](images/upgrade.png)

## PrivEsc to Vianka

> Use `linenum` to find linux privilage escalation routes. On this machine, `xxd` is an `SUID binary`.

![](images/linenum.png)

> Exploit `xxd` to `read /etc/shadow` and `/etc/passwd` and `save` both to files

![](images/vianka.png)  

![](images/unshadow.png)

> Crack the `unshadow.txt` file

![](images/cracked.png)

## User Flag

![](images/userflag.png)

## PrivEsc to Root

> Use the same exploit to read the `/etc/sudoers` file and `copy` it to a new file

![](images/sudoers.png)

> `Add vianka` to the `new sudoers file` and `overwrite` the original, then switch to root. 

![](images/root.png)

## Root Flag

![](images/rootflag.png)
