# gallery

![](https://images.unsplash.com/photo-1510127034890-ba27508e9f1c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80)

---

## nmap

![](images/nmap.png)  

## ffuf

> /gallery/ directory

![](images/gallery.png)  

> requires login

![](images/login.png)  

## sql injection

> sending a login request in burp shows the sql query

![](images/sqli.png)  

> `') or 1=1#` allows for successful login

![](images/success.png)  

## exploit

> use this exploit to generate a rce payload

![](images/exploit.png)

![](images/rce.png)  

## reverse shell

> capture the request and pass it into burp, the machine doesnt have python to upgrade the tty, so encode a socat reverse shell and send it

![](images/burpsocat.png)  

> with a socat listener open to get an interactive shell

![](images/socat.png)  

## database

> the database initialize.php file contains the mysql login credentials

![](images/dblogin.png)  

> use mysql to get the admin's password hash

## PrivEsc

> linpeas found a mike user with the user flag

![](images/mike.png)  

> linpeas found mikes password in his history

![](images/password.png)  

## User

![](images/mikelogin.png)  

## User flag

![](images/userflag.png)  

## PrivEsc to root

> mike can run the following script as sudo

![](images/sudo.png)  


## Root

> run the script, select to read it, then exploit nano to get root


## Root flag

![](images/rootflag.png)  




