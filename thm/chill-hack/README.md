# Chill Hack

![](https://tryhackme-images.s3.amazonaws.com/room-icons/897a124df0a70ad86502193b83f46658.png)

## Rustscan

![](images/rustscan.png)  

## ffuf

![](images/ffuf.png)  

 > /secret has a command execution form

 ![](images/secret.png)  

 > some commands are restricted

 ![](images/nonono.png)  

 > using \ to bypass the filter works

 ![](images/bypass.png)  

 > blacklisted commands are in the source
 
 ![](images/blacklist.png)  

## Reverse shell

> make a file with a reverse shell in it, open a http server and download and execute it on the website

![](images/rs.png)  

![](images/curlsh.png)  

## www-data

> sudo -l shows that www-data can run a helpline script as apaar, inject /bin/bash into the second line to get a shell as apaar

![](images/apaar.png)  

## Local flag

![](images/userflag.png)  

## PrivEsc

> download the image in the /files/images folder in /var/html

![](images/hackerwithalaptop.png)  

> use stegseek to find the zip file, use zip2john to crack the hash to the passphrase

![](images/zip.png)  

> use the passphrase to download source_code.php 

![](images/source.png)  

## User 

> use the credentials in the source code file to SSh as anurodh

![](images/sshanurodh.png)  

## Root

> Anurodh is in the docker group, exploit docker to get root.

![](images/root.png)  

## Root flag

![](images/rootflag.png)  



