# Mr Robot CTF
![](https://i.imgur.com/Bo6jUIK.png)

---

## nmap

> Web server is running, lets check it out.

![](images/nmap.png)

> Seems to be a shell/terminal application.

![](images/website.png)

## ffuf
 Let's scan for files and directories using ffuf.

![](images/ffuf.png)

> Notably, ffuf discovered **robots.txt**, which given the name of the CTF, I think is a priority here.

## Key 1

![](images/robots.png)


# Key 2

> For this key, I'll be focussing my attention on the wordpress login form that we found when fuzzing ('/**login**').

![](images/login.png)

## WPScan

> First, we need to get the login. I'm going to use the dictionary file referred to in the robots .txt file ('**fsocity.dic**') to find the username. But it has some duplicates, so I need to remove those:

![](images/wpscan.png)

> We found **Elliott**, now to find his password. I'm going to use the same dictionary to attack the password field.

![](images/elliott.png)

> Found it!

![](images/found.png)

## Reverse Shell

> Now that we've logged in, as you can see here, in the dashboard we are able to edit php files, thus allowing us to upload and run a reverse shell.
 
![](images/reverse.png)

> Open a netcat listener

![](images/netcat.png)

> Run the compromised file

![](images/compromised.png)

> Get and upgrade shell

![](images/upgrade.png)

> get key #2

![](images/key2.png)

> we can't!

![](images/cant.png)

> we need to escalate our privelages to root.

# PrivEsc
Search for setuid binaries:

![](images/setuid.png)

> We're going to abuse the nmap binary to get root

![](images/root.png)

## Keys 2 and 3

> We can now read key2

![](images/key2yes.png)

> And key3

![](images/key3.png)

