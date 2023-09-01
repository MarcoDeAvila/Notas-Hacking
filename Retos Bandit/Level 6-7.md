# Level 6-7
## Objetivo

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit6
> **Password:** P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit6@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit6@bandit.labs.overthewire.org's password:
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Apr 23 18:04 .
drwxr-xr-x 70 root root 4096 Apr 23 18:05 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit6@bandit:~$ find / -user bandit7--group bandit6 -size 33c 2>/dev/null
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```

**Password encontrado:** z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
## Notas adicionales

|Comando | Descripción |
|-|-|
|group| archivo de grupo de usuarios.|
## Referencias