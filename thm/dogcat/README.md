# dogcat

![](https://tryhackme-images.s3.amazonaws.com/room-icons/ce2fe16cfcdac475834f262306243b0a.png)

---

## nmap

![](images/nmap.png)

> When the button is pressed either a dog or cat is displayed with the parameter in the URL.

![](images/website.png)

> But, it only allows us to access cats or dogs

![](images/site.png)

> However, we can use `php filter bypasses` such as `b64 encoding` to get around this:

![](images/access.png)

> By decoding the base64 the raw `index.php` code is revealed. Data can be passed to the `ext` variable to read any file of any extension.

![](images/decrypt.png)

![](images/ext.png)

> Using the same method, the Apache2 log file `access.log` can be accessed.

![](images/logs.png)

> Capture and send the request to BurpSuite

![](images/request.png)


> Exploit `RCE` using the php in the `user-agent`

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

> Use `sudo -l` to list all programs that can be run as root, and exploit `env` to get a bash shell

![](images/sudol.png)

![](images/root.png)

## Flag 3

![](images/flag3.png)

## docker PrivEsc

> Run ```cat/proc/1/cgroup```, the room is in a docker container

![](images/cgroup.png)

> In the `/opt/backups` folder, `backup.sh` is being backed up every minute.

![](images/backups.png)

> Overwrite `backup.sh` to get a reverse shell

![](images/overwrite.png)

> Append the reverse shell onto `backup.sh` and wait for the cronjob to execute it to get a shell.

![](images/reverse.png)

## Flag 4

![](images/flag4.png)
