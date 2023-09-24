# Level 26-27
## Objetivo
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit26
> **Password:** c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit26@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit26@bandit.labs.overthewire.org's password:
  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
Connection to bandit.labs.overthewire.org closed.

------------ Entramos desde el MORE --------------------------

 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
:shell
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ ./bandit27-do
Run a command as another user.
  Example: ./bandit27-do id
bandit26@bandit:~$ cat text.txt
  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
```

**Password encontrado:** YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
## Notas adicionales

Segui un videotutorial para resolver este reto, la solucion se basaba en entrar al servidor de bandit 26 desde el "more" y ejecutar estos comandos.

:set shell=/bin/bash
:shell

De esta forma entrabamos a bandit26.
## Referencias

[(21) OverTheWire | Bandit (Nivel 26-27) - YouTube](https://www.youtube.com/watch?v=kJxNXv6_-x8&list=PLuYfa_nCnOPURyDp4aDT4TIhKr2XqxgLd&index=11)