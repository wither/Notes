# mustacchio

![](https://tryhackme-images.s3.amazonaws.com/room-icons/9150a15223eb72f053804a3975133e3d.png)

---

## nmap

![](images/nmap.png)  

## users

> the webserver has a file called 'users.bak' in a custom js folder.

![](images/users.png)  

> it contains some SQL admin credentials

![](images/creds.png)  

> crack the password 

## admin panel

> theres an admin panel on :8765 login with the admin credentials

![](images/login.png)  

> after logging in theres a comment box

![](images/comment.png)  

## xxe

> which sends the comment as xml

![](images/xml.png)  

> theres a comment in the source about a /auth/dontforget.bak, which contains a comment example in the form of xml

![](images/dontforget.png)  

> sending the xml comment displays it in the response

![](images/xmlformat.png)  

> use xxe lfi to get barry's ssh key

![](images/xxelfi.png)  

## User

> pass the id_rsa to ssh2john, crack it to get the passphrase and ssh into the machine as barry

![](images/shs.png)  

## User flag

![](images/userflag.png)  

## PrivEsc

> binary in joes home folder has suid perms

![](images/livelog.png)  

> download it

![](images/scp.png)  

> it tails the access log

## Root flag

> add barrys home to PATH and write a command to a tails file, so that when live_log is ran, tails is ran as root

![](images/rootflag.png)  

