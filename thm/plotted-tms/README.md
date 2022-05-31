# plotted-tms

![](https://tryhackme-images.s3.amazonaws.com/room-icons/6187c9220cd0ff0c5c3b29b9aa6252ea.png)

---

## Nmap

![](images/nmap.png)  

## Ffuf

> Nothing found on `:80`, but found `/management/ `on `:445`

![](images/443.png)  

## Website

> It's a login page

![](images/website.png)   

## Exploit

> Use this exploit to upload an `RCE` payload

![](images/exploit.png)  

![](images/rce.png)  

## Reverse shell

> Send a `URL encoded` netcat reverse shell with a listener open to get a reverse shell

![](images/rs.png)  

![](images/rsnc.png)  

## PrivEsc

> `plot_admin` is the other user

![](images/plot_admin.png)  

> `backup.sh` is being run as `plot_admin` in `/etc/crontab`

![](images/crontab.png)  

> `backup.sh`

![](images/backup.png)  

## User

> Delete `backup.sh`, and make a new one that spawns a reverse shell, wait for it to be ran as `plot_admin` by the cronjob

![](images/user.png)  

## User flag

![](images/userflag.png)  

## PrivEsc

> `openssl` can be ran as root using `doas`, exploit that to add another root user to `/etc/passwd`

`LFILE=/etc/passwd`
`echo "wither:$1$wither$HlLgmlz4PVTP7kcFAbgRt0/:0:0:/root/root:/bin/bash" | doas -u root openssl enc -out "$LFILE"`
