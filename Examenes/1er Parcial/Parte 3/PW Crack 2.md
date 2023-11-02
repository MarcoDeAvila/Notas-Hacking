# PW Crack 2
## Objetivo

Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Solución

```shell
tux3000-picoctf@webshell:~$ ls
README.txt  level2.flag.txt.enc  level2.py
tux3000-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: Tux3000
That password is incorrect
tux3000-picoctf@webshell:~$ nano level2.py
tux3000-picoctf@webshell:~$ python 
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)
'de76'
>>> 
tux3000-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
tux3000-picoctf@webshell:~$ 
```
## Notas adicionales
## Referencias