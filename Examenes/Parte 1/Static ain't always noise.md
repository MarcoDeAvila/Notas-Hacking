# Static ain't always noise
## Objetivo

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static)? This [BASH script](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh) might help!
## Solución

```shell
tux3000-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static
2023-09-25 17:14:10 (224 MB/s) - 'static' saved [8376/8376]
tux3000-picoctf@webshell:~$ ls -l
total 20
-rw-r--r-- 1 root            root            4443 Sep 25 16:51 README.txt
-rw-rw-r-- 1 tux3000-picoctf tux3000-picoctf 8376 Mar 16  2021 static
tux3000-picoctf@webshell:~$ chmod +x static 
tux3000-picoctf@webshell:~$ ./static 
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
tux3000-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_98d35619}
tux3000-picoctf@webshell:~$ 
```
## Notas adicionales
## Referencias