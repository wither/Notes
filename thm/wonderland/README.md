# Wonderland
![](https://i.imgur.com/q9N2UUs.png)

## nmap

![](images/nmap.png)

## fuff

![](images/ffuf.png)

> Use ffuf to find a folder tree called /r/a/b/b/i/t, leads to

![](images/rabbit.png)

> In the source of this page, theres a hidden message containing ssh credentials

![](images/sshcreds.png)

## User

> Login with credentials

![](images/sshlogin.png)

## Privilege Escalation

> Rabbit can run the python script found in the home directory as root
the script uses the random module, create a random.py to import

![](images/random.png)

## User 2

> Now the rabbit user

![](images/rabbituser.png)

> Theres a binary called teaparty in rabbits home directory that outputs this when run

![](images/output.png)

> Download teaparty using netcat

![](images/download.png)

![](images/teapartyrun.png)

> Use strings to see the source, it uses 'date' using a path variable

![](images/strings.png)

## User 3

> Make a new directory in rabbits home, make a file called date and add the directory to the PATH variable, so that when 'date' is called in teaParty, it executes the file instead

![](images/path.png)

### Root

> hatters password is in their home directory

![](images/hatters.png)

> Use getcap to list binaries with capabilities set

![](images/getcap.png)

> After switching to the hatter user, use gtfobins' perl capabilities payloads to get root

![](images/perlcap.png)

## Flags!

> Capture them

![](images/flags.png)
