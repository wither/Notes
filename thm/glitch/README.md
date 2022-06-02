# glitch

![](https://tryhackme-images.s3.amazonaws.com/room-icons/baebc18318f328bf978120cde5328cb0.jpeg)

---

## Rustscan

> `:80 is open`

![](images/rust.png)  

## API

> Website has an endpoint called `access` in the source

![](images/access.png)  

## Flag 1 

> The first flag is the token found at the endpoint base64 decoded

![](images/flag1.png)  

## API

> Fuzz the API to find `/api/items` 

 ![](images/ffuf.png)  

> Which contains sins, errors and deaths.

![](images/items.png) 

> Change `GET` to `POST` in `BurpSuite` to get a message. 

![](images/glitch.png) 

> `/api/items` takes a `cmd` parameter

![](images/cmd.png)  

## User

> Send a URL encoded reverse shell as the cmd with a listener open to get user shell

![](images/shellburp.png)  

![](images/userflag.png)  

## PrivEsc

> Theres a hidden folder called `.firefox` containing firefox data in `/home/user`

![](images/firefox.png)  

> Archive it and send it via to analyze

![](images/netcathost.png)  

![](images/netcatattack.png)  

> Unzip the folder and use `firefox-decrypt.py` to dump the firefox data, getting a `v0id` user and password.

![](images/firefoxdecrypt.png)  

## User v0id

> Login with the credentials found in firefox

![](images/v0idlogin.png)  

## PrivEsc to root

> `v0id` can run `doas` as root

![](images/doas.png)  

> Start bash as root using `doas`

![](images/root.png)  


