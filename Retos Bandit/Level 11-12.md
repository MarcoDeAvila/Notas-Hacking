# Level 11-12
## Objetivo

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.
## Datos de acceso al nivel

> [!IMPORTANT]
> **Host:** bandit.labs.overthewire.org
> **User:** bandit11 
> **Password:** 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
> **Port:**  2220
## Solución

```shell
C:\Users\Marco De Avila>ssh bandit11@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit11@bandit.labs.overthewire.org's password:
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$
```

**Password encontrado:** JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Notas adicionales

|Comando | Descripción|
|-|-|
|tr| Permite el remplazo o eliminación de un conjunto de caracteres de la entrada estándar.|
|Rot13| Es un cifrado de sustitución de letras simple que reemplaza una letra con la letra 13 después de ella en el alfabeto latino.|

Existe otra forma de solucionar este reto, la solución se obtiene al utilizar Python con el modulo **codecs**.
## Referencias

[ROT13 - Wikipedia, la enciclopedia libre](https://en.wikipedia.org/wiki/ROT13)