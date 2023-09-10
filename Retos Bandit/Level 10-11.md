# Level 10-11
## Objetivo

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit10
> **Password:** G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit10@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit10@bandit.labs.overthewire.org's password:
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "Hola Mundo"
Hola Mundo
bandit10@bandit:~$ echo "Hola Mundo" | base64
SG9sYSBNdW5kbwo=
bandit10@bandit:~$ echo -n SG9sYSBNdW5kbwo= | base64 -d
Hola Mundo
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```

**Password encontrado:** 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
## Notas adicionales

|Comando | Descripción |
|-|-|
|base64|Base64 es un grupo de esquemas de codificación binaria a texto que representan datos binarios.|
## Referencias

[Base64 - Wikipedia, la enciclopedia libre](https://en.wikipedia.org/wiki/Base64)