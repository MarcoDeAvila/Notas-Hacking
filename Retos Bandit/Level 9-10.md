# Level 9-10
## Objetivo

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit9 
> **Password:** EN632PlfYiZbn3PhVK3XOGSlNInNE00t
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit9@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit9@bandit.labs.overthewire.org's password:
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
```

**Password encontrado:**  G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
## Notas adicionales

|Comando | Descripción |
|---|---|
|strings|imprimir las secuencias de caracteres imprimibles en archivos.|
## Referencias