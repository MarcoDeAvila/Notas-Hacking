# Level 1-2
## Objetivo

The password for the next level is stored in a file called **-** located in the home directory.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit1
> **Password:** NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit1@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit1@bandit.labs.overthewire.org's password:
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

**Password encontrada:** rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
## Notas adicionales

## Referencias