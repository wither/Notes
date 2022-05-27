# Wonderland
![](https://i.imgur.com/q9N2UUs.png)

## nmap

![](images/nmap.png)

## fuff

![](images/ffuf.png)

> found a folder tree called /r/a/b/b/i/t, leads to:

![](images/rabbit.png)

> In the source of this page, theres a hidden message containing ssh credentials

![](images/sshcreds.png)

## User

> worked

![](images/sshlogin.png)

## Privilege Escalation

> rabbit can run the python script found in the home directory as root
the script uses the random module, create our own random.py to import

![](images/random.png)

## User 2

> now the rabbit user

![](images/rabbituser.png)

> theres a binary called teaparty in rabbits home directory

![](images/teaparty.png)

> get this when ran

![](images/output.png)

> download teaparty using netcat

![](images/download.png)

![](images/teapartyrun.png)

> using strings we can see the source, it uses 'date' using a path variable maybe its overwritable

![](images/strings.png)

## User 3

> make a new directory in rabbits home, make a file called date and add the directory to the PATH variable, so that when 'date' is called in teaParty, it executes the file instead

![](images/path.png)
![[Pasted image 20220515233145.png]]

### Root

> hatters password is in their home directory

![](images/hatters.png)

> Using getcap we can list binaries with capabilities set, these can be exploited

![](images/getcap.png)

> after switching to the hatter user, using gtfobins' perl capabilities line we can get root

![](images/perlcap.png)

## Flags!

get em

![](images/flags.png)
