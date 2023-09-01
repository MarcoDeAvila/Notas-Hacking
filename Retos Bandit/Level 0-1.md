# Level 0-1
## Objetivo

The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit0
> **Password:** bandit0
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit0@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password:
bandit0@bandit:~$ whoami
bandit0
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$
```

**Password encontrada:** NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
## Notas adicionales

|Comando | Descripción |
|----------|----------|
| pwd | *Me indica el directorio actual* |
| whoami | *Me indica el usuario actual* |
| ls | Me listar el contenido del directorio |
| cat | Concatena archivos e imprimir en la salida estándar |

## Referencias