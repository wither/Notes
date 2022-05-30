# agent-sudo

![](https://tryhackme-images.s3.amazonaws.com/room-icons/aedc6b66c222e15ff740c282a0c3f44e.png)

---

## nmap

![](images/nmap.png)  

## codename

> Website says to use codename as the user-agent to access more

![](images/codename.png)  

## burpsuite

> R as the user-agent discloses there are 25 other employees, 1 for each letter of the alphabet.

 ![](images/R.png)  

> use intruder to bruteforce the codename

![](images/setting.png)   

![](images/position.png) 

## agent C

> user-agent:C redirects to agent_C_attention.php

![](images/agentC.png)  

> that file reads this, chris agent C's username

![](images/chris.png)  

## hydra

> bruteforce chris's ftp password

![](images/ftppass.png)  

## ftp

> login and download the .txt file

![](images/toagentj.png)  

> Agent J's password is somewhere in the images

![](images/image.png)  

> Download the images

![](images/downloadaliens.png) 

## Steganography

>  use stegseek to view the steganographic within one of the files, it gives us a name and password that we can login to via ssh

![](images/stegseek.png)  

## User flag

![](images/userflag.png)  

## PrivEsc

> Use CVE-2019-14287 to escalate privilages

![](images/root.png)  

## Root flag

![](images/rootflag.png)  