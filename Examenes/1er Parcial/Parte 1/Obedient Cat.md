# Obedient Cat
## Objetivo

This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/2d24d50b4ebed90c704575627f1f57b2/flag).
## Solución

```shell
tux3000-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/2d24d50b4ebed90c704575627f1f57b2/flag
--2023-09-25 16:52:26--  https://mercury.picoctf.net/static/2d24d50b4ebed90c704575627f1f57b2/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag 100%[=========================================>]      34  --.-KB/s    in 0s      

2023-09-25 16:52:26 (24.5 MB/s) - 'flag' saved [34/34]

tux3000-picoctf@webshell:~$ ls
README.txt  flag  warm
tux3000-picoctf@webshell:~$ cat flag 
picoCTF{s4n1ty_v3r1f13d_f28ac910}
tux3000-picoctf@webshell:~$
```
## Notas adicionales
## Referencias