# PW Crack 3
## Objetivo

Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución

```shell
tux3000-picoctf@webshell:~$ ls
README.txt  level3.flag.txt.enc  level3.hash.bin  level3.py
tux3000-picoctf@webshell:~$ nano level3.py 
tux3000-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: f09e
That password is incorrect
tux3000-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 4dcf
That password is incorrect
tux3000-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
tux3000-picoctf@webshell:~$ 
```
## Notas adicionales

Revisando el script level3.py encontré las posibles contraseñas.
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]
## Referencias