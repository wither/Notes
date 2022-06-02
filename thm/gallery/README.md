# gallery

![](https://tryhackme-images.s3.amazonaws.com/room-icons/c53a8eb73f24535345477fdf603fe1de.png)

---

## Nmap

![](images/nmap.png)  

## Ffuf

> `/gallery/` directory

![](images/gallery.png)  

> It requires a login

![](images/login.png)  

## SQL Injection

> Sending a login request in `BurpSuite` shows the SQL query

![](images/sqli.png)  

> `') or 1=1#` allows for successful login.

![](images/success.png)  

## Exploit

> Use this exploit to generate a `RCE` payload

![](images/exploit.png)

![](images/rce.png)  

## Reverse shell

> Capture the request and pass it into `BurpSuite`, encode reverse shell and send the request.

![](images/burpsocat.png)  

> Have a listener open to get an interactive shell

![](images/socat.png)  

## Database

> The database `initialize.php` file contains the MySQL login credentials.

![](images/dblogin.png)  

> Use `mysql` to get the admin's password hash

## PrivEsc

> `linpeas` found a `mike` user with the user flag

![](images/mike.png)  

> `linpeas` found `mike`'s password in his `.bash_history`

![](images/password.png)  

## User

![](images/mikelogin.png)  

## User flag

![](images/userflag.png)  

## PrivEsc to root

> `mike` can run the following script as sudo:

![](images/sudo.png)  


## Root

> Run the script, select to `read` it, then exploit `nano` to get root.


## Root flag

![](images/rootflag.png)  




