# agent-sudo

![](https://tryhackme-images.s3.amazonaws.com/room-icons/aedc6b66c222e15ff740c282a0c3f44e.png)

---

## Nmap

![](images/nmap.png)  

## Codename

> The website says to use a codename as the `user-agent` to access more.

![](images/codename.png)  

## Burpsuite

> `R` as the `user-agent` discloses there are 25 other employees (1 for each letter of the alphabet)

 ![](images/R.png)  

> Use `BurpSuite`'s `intruder` tool to bruteforce the codename.

![](images/setting.png)   

![](images/position.png) 

## Agent C

> `user-agent:C` redirects to `agent_C_attention.php`

![](images/agentC.png)  

> `agent_C_attention.php` reads this:

![](images/chris.png)  

## Hydra

> Use `hydra` to bruteforce `chris`'s FTP password

![](images/ftppass.png)  

## ftp

> Login and download the `To_agentJ.txt` file

![](images/toagentj.png)  

> Agent J's password is somewhere in the images

![](images/image.png)  

> Download the images.

![](images/downloadaliens.png) 

## Steganography

>  Use `stegseek` to view the steganographic data within `cute-alien.jpg`, ireavealing a name and password that we can login to via SSH.

![](images/stegseek.png)  

## User flag

![](images/userflag.png)  

## PrivEsc

> Use `CVE-2019-14287` to escalate privilages to root.

![](images/root.png)  

## Root flag

![](images/rootflag.png)  