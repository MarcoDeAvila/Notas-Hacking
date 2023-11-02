# Fixme1.py
## Objetivo

Fix the syntax error in this Python script to print the flag.
[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## Solución

```shell
tux3000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/26/fixme1.py
tux3000-picoctf@webshell:~$ ls
README.txt  fixme1.py
tux3000-picoctf@webshell:~$ python fixme1.py 
  File "/home/tux3000-picoctf/fixme1.py", line 13
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
tux3000-picoctf@webshell:~$ nano fixme1.py 
tux3000-picoctf@webshell:~$ python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
tux3000-picoctf@webshell:~$ 
```
## Notas adicionales

Se corrigió la indentacion del print( ).
## Referencias