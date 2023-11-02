# PW Crack 1
## Objetivo

Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## Solución

```shell
tux3000-picoctf@webshell:~$ ls
README.txt  level1.flag.txt.enc  level1.py
tux3000-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: Tux3000
That password is incorrect
tux3000-picoctf@webshell:~$ nano level1.py 
tux3000-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
tux3000-picoctf@webshell:~$ 
```
## Notas adicionales

Revise el script level1.py con un nano y ahí encontré la contraseña.
## Referencias