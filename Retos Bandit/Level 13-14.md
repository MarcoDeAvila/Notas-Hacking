# Level 13-14
## Objetivo

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit13
> **Password:** wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit13@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit13@bandit.labs.overthewire.org's password:
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes


bandit14@bandit:~$ ls
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ exit
logout
Connection to localhost closed.
bandit13@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```

**Password encontrado:** fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
## Notas adicionales

| Termino | Descripción |
|-|-|
| Clave publica | La **clave pública**, como su nombre indica, es **pública** y se debe distribuir a quienes desean comunicarse con nosotros. Tanto si sirve para cifrar mensajes como para comprobar la autenticación.|
| Clave privada |  La **clave privada** no debe distribuirse a nadie, y sirve para descifrar el mensaje que ha sido cifrado con la **clave pública**.|
## Referencias

[Clave pública y clave privada para cifrar datos - ICM](https://www.icm.es/2021/12/05/clave-publica-clave-privada-cifrado-de-datos/#:~:text=La%20clave%20p%C3%BAblica%2C%20como%20su,cifrado%20con%20la%20clave%20p%C3%BAblica.)