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
>>>>>>> d42aefa (change tense)

![](images/useragent.png)

> Execute a remote shell using the same technique:

![](images/shell.png)

<<<<<<< HEAD
> Get shell!

![](images/shellsuccess.png)

> Get Flag1
=======
## nc

> Run a netcat listener and get a shell

![](images/shellsuccess.png)

## Flag 1
>>>>>>> d42aefa (change tense)

![](images/flag1.png)

## Flag 2

<<<<<<< HEAD
> Get flag2

![](images/flag2.png)

## Flag 3

> Use sudo -l to list all programs that we can run as root, and use env to get a bash shell

![](images/sudol.png)

> we are root!

![](images/root.png)

> get flag3

![](images/flag3.png)

## Flag 4

> Using cat/proc/1/cgroup we can see that we are in a docker container

![](images/cgroup.png)

> in the /opt/backups folder,backup.sh is being backed up every minute

![](images/backups.png)

> we can overwrite backup.sh to get a reverse shell
=======
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
>>>>>>> d42aefa (change tense)

![](images/overwrite.png)

> Append the reverse shell onto the file and wait for it to execute to get a shell

![](images/reverse.png)

<<<<<<< HEAD
> get flag4!
=======
## Flag 4
>>>>>>> d42aefa (change tense)

![](images/flag4.png)
