# Mr Robot CTF
![](https://tryhackme-images.s3.amazonaws.com/room-icons/7a8797ae59733f2a72f0e8a8748be128.jpeg)

---

## nmap

![](images/nmap.png)

## ffuf

>  Scan the url using ffuf

![](images/ffuf.png)

> Notably, ffuf will discover **robots.txt**

## Key 1

![](images/robots.png)

## WPScan

> ffuf will also find a wordpres login form. Use the dictionary file referred to in the robots.txt file ('**fsocity.dic**') to find the username. Remove those.

![](images/wpscan.png)

> Get the user "**Elliott**"

![](images/elliott.png)

> Get his password

![](images/found.png)

## Reverse Shell

> Edit the php theme to upload and run a reverse shell.
 
![](images/reverse.png)

> Open a netcat listener

![](images/netcat.png)

> Run the compromised file

![](images/compromised.png)

> Get and upgrade shell

![](images/upgrade.png)

# PrivEsc

> Search for setuid binaries

![](images/setuid.png)

> Abuse the nmap binary to get root

![](images/root.png)

## Key 2 

![](images/key2yes.png)

## Key 3

![](images/key3.png)


