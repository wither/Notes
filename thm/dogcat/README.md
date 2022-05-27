# dogcat

![](https://i.imgur.com/nSkIlFr.png)

---

## nmap

> It's running an Apache webserver, lets check it out

![](images/nmap.png)

> You press a button and either a dog or cat is displayed with the parameter in the URL.

![](images/website.png)

> But, it only allows us to access cats or dogs

![](images/site.png)

> However, we can use php filter bypasses such as b64 encoding to get around this:

![](images/access.png)

> As you can see, by decoding the base64 we get the raw index.php code. As you can see in the code, the "**ext**" variable can be set, meaning we could in theory read any file of any extension. Lets try read /etc/passwd

![](images/decrypt.png)

![](images/ext.png)

> Using the same method, we can access the apache2 log files

![](images/logs.png)

> capture and send the request in burpsuite

![](images/request.png)

> rce using the php in the user agent
=======
=======
>>>>>>> e19cf64 (tense)
![](images/nmap.png)

## Website

> Display dog or cat with button

![](images/website.png)

> Only allows cats or dogs

![](images/site.png)

> Use php filter bypasses such as b64 encoding to get around this

![](images/access.png)

> Get the raw index.php code by decoding the base64.

![](images/decrypt.png)

> The "**ext**" variable can be set, meaning file of any extension can be read. For example, /etc/passwd.

![](images/ext.png)

> Access the apache2 log files using the same method

![](images/logs.png)

## burpsuite

> Capture and send the request in burpsuite

![](images/request.png)

> Exploit RCE using the php in the user agent

![](images/useragent.png)

> Execute a remote shell using the same technique:

![](images/shell.png)

## nc

> Run a netcat listener and get a shell

![](images/shellsuccess.png)

## Flag 1

![](images/flag1.png)

## Flag 2

![](images/flag2.png)

## PrivEsc

> Use sudo -l to list all programs that can be run as root, and use env to get a bash shell

![](images/sudol.png)

![](images/root.png)

## Flag 3

![](images/flag3.png)

## docker PrivEsc

> Run ```cat/proc/1/cgroup```, the room is in a docker container

![](images/cgroup.png)

> In the /opt/backups folder, backup.sh is being backed up every minute

![](images/backups.png)

> Overwrite backup.sh to get a reverse shell

![](images/overwrite.png)

> Append the reverse shell onto the file and wait for it to execute to get a shell

![](images/reverse.png)

## Flag 4

![](images/flag4.png)
