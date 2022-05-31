# mustacchio

![](https://tryhackme-images.s3.amazonaws.com/room-icons/9150a15223eb72f053804a3975133e3d.png)

---

## Nmap

![](images/nmap.png)  

## Users

> The webserver has a file called `users.bak` in a `/custom/js/` folder.

![](images/users.png)  

> It contains some SQL admin credentials

![](images/creds.png)  

> Crack the password 

## Admin panel

> Theres an admin panel on `:8765`, login with the admin credentials.

![](images/login.png)  

> After logging in theres a comment box

![](images/comment.png)  

## XXE

> Which sends the comment as `xml`

![](images/xml.png)  

> Theres a comment in the source about a `/auth/` dont `forget.bak`, which contains a comment example in the form of `xml`.

![](images/dontforget.png)  

> Sending the `xml` comment displays it in the response

![](images/xmlformat.png)  

> Use `XXE` `LFI` to get `barry`'s SSH key

![](images/xxelfi.png)  

## User

> Pass the `id_rsa` to `ssh2john`, crack it to get the passphrase and ssh into the machine as `barry`.

![](images/shs.png)  

## User flag

![](images/userflag.png)  

## PrivEsc

> There's a binary in the `joes/home/` folder has `suid` permissions

![](images/livelog.png)  

> Download it using `scp`

![](images/scp.png)  

> it `tail`s the access log

## Root flag

> Add `barry`'s home to `$PATH `and write a command to a `tail` file, so that when `live_log` is ran, `tail` is also ran as root.

![](images/rootflag.png)  

