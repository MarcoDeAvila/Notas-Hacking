# Level 7-8
## Objetivo

The password for the next level is stored in the file **data.txt** next to the word **millionth**.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit7
> **Password:** z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit7@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit7@bandit.labs.overthewire.org's password:
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ wc data.txt
  98567  197133 4184396 data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```

**Password encontrado:** TESKZC0XvTetK0S9xNwm25STk5iWrBvP
## Notas adicionales

|Comando| Descripción |
|---|---|
|wc| imprimir recuentos de nuevas líneas, palabras y bytes para cada archivo|
|grep | imprimir líneas que coincidan con los patrones|
## Referencias