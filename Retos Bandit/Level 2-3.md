# Level 2-3
## Objetivo

The password for the next level is stored in a file called **spaces in this filename** located in the home directory.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit2
> **Password:** rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit2@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit2@bandit.labs.overthewire.org's password:
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```

**Password encontrada:** aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
## Notas adicionales

## Referencias