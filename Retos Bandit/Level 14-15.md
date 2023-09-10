# Level 14-15
## Objetivo

The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit14
> **Password:** fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit14@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit14@bandit.labs.overthewire.org's password:
bandit14@bandit:~$ ls
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

^C
bandit14@bandit:~$
```

**Password encontrado:** jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Notas adicionales

| Comando | Descripción |
|-|-|
| nc | El comando Netcat (**`nc`**) es una utilidad de línea de comandos para leer y escribir datos entre dos redes de equipos. La comunicación se realiza mediante TCP o UDP. El comando difiere según el sistema (**`netcat`**, nc, **`nc`** y otros).|
## Referencias

[Comando nc (Netcat): sintaxis, opciones de comando y ejemplos (phoenixnap.com)](https://phoenixnap.com/kb/nc-command#:~:text=The%20Netcat%20(%20nc%20)%20command%20is,using%20either%20TCP%20or%20UDP.)