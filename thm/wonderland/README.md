# Wonderland
![](https://tryhackme-images.s3.amazonaws.com/room-icons/fdba6eaf85513262b2a9b12875b0f342.jpeg)

---

## Nmap

![](images/nmap.png)

## Fuff

![](images/ffuf.png)

> Use ffuf to find a folder tree called `/r/a/b/b/i/t`, leads to

![](images/rabbit.png)

> In the source of this page, theres a hidden message containing SSH credentials

![](images/sshcreds.png)

## User

> Login with the credentials

![](images/sshlogin.png)

## Privilege Escalation

> `rabbit` can run the python script `walrus_and_the_carpenter.py` found in the `/home/alice` directory as root
the script uses the random module, create a `random.py` to import

![](images/random.png)

## User 2

> Now the rabbit user

![](images/rabbituser.png)

> Theres a binary called `teaParty` in `rabbit`'s `/home` directory that outputs this when run:

![](images/output.png)

> Download `teaParty` using `netcat`

![](images/download.png)

![](images/teapartyrun.png)

> Use `strings` to see the source, it refernces `date` using a PATH variable.

![](images/strings.png)

## User 3

> Make a new directory in `rabbit`'s home, make a file called `date` and add the directory to the `PATH` variable, so that when `date` is called in `teaParty`, it executes the file instead.

![](images/path.png)

### Root

> `hatter`'s password is in their `/home` directory

![](images/hatters.png)

> Use `getcap` to list binaries with `capabilities` set

![](images/getcap.png)

> After switching to the `hatter` user, use gtfobins' `perl` `capabilities` payloads to get root

![](images/perlcap.png)

## Flags!

> Capture them

![](images/flags.png)
