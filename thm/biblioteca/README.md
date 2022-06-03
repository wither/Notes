# Biblioteca [Medium]

![](https://tryhackme-images.s3.amazonaws.com/room-icons/234e64423ae186a73cc9f905522a0f46.png)

---

## Rustscan

![](images/rustscan.png)  

## Website

> Site is a login form

![](images/site.png)  

## Burp

> seems to be vulnerable to simple SQLi, get a login and a user 'smokey'

![](images/sqli.png)  

> username is in column 2

![](images/2.png)  

> found the website database

![](images/websitedb.png) 

> query the users table to find password column

![](images/userstable.png)  

> Get smokey's password

![](images/password.png)  

## User

> ssh in as smokey

![](images/user.png)  

## PrivEsc

> theres another user called hazel, their password is very easy to guess

![](images/hazel.png)  

> hazel can set the python environment variable as well as run hasher.py as root. hasher.py uses a library called hashlib

![](images/hasher.png)  

## Root

> make a hashlib.py in /tmp to spawn a bash shell, sudo set the python environment variable to /tmp and run hasher.py. Wait for hasher.py to import and execute the malicious library to get root

![](images/root.png)  

## Root flag

![](images/rootflag.png)  