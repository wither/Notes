# nax

![](https://i.imgur.com/GF8Xhq5.png)

---

## nmap

![](images/nmap.png)  

## Website

> not much to the website at first glance, however there are some elements.

![](images/website.png)  

## Secret file

> I wrote a python program to take the elements and convert each one to their corresponding periodic number, then that number to ascii to get the path to the secret file.

![](images/piet.png)  

> when I go to that path, this is the image

![](images/weirdimage.png)  

> using wget and exiftool (https://www.exiftool.org/install.html#Unix), we can download and view the metadata of the file 

![](images/exiftool.png)  


> after converting it to ppm, we can use npiet (https://www.bertnase.de/npiet/) to interpret the file into readable text, revealing a username and password.

![](images/npiet.png)  


## Exploit

> using the username and password as well as authenticated rce in metasploit we can get a meterpreter shell 

![](images/meterpreter.png)  

## User flag

![](images/userflag.png)  

## Root flag

![](images/rootflag.png)  




