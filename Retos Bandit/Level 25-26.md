# Level 25-26
## Objetivo

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit25
> **Password:** p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit25@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit25@bandit.labs.overthewire.org's password:
cat /etc/passwd | grep bandit26
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p 2220
--------- Nueva Ventana de Linea de Comando ------------------------
 
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```

**Password encontrado:** c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
## Notas adicionales

No comprendí el material de la clase pero seguí un video para resolverlo, la solución se basaba en abrir una nueva conexión al bandit26 pero quedarnos en "more" y ejecutar el siguiente comando.

:r /etc/bandit_pass/bandit26
## Referencias

[(21) OverTheWire | Bandit (Nivel 25) - YouTube](https://www.youtube.com/watch?v=JKkQw8C0cY8&list=PLuYfa_nCnOPURyDp4aDT4TIhKr2XqxgLd&index=10)