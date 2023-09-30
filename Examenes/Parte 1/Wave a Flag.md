# Wave a Flag
## Objetivo

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm) has extraordinarily helpful information...
## Solución

```shell
tux3000-picoctf@webshell:~$ ls -la
total 44
drwxr-xr-x 2 tux3000-picoctf tux3000-picoctf   138 Sep 25 16:40 .
drwxr-xr-x 3 root            root               29 Sep 25 16:29 ..
-rw------- 1 tux3000-picoctf tux3000-picoctf    30 Sep 25 16:29 .bash_history
-rw-r--r-- 1 tux3000-picoctf tux3000-picoctf   220 Sep 25 16:29 .bash_logout
-rw-r--r-- 1 tux3000-picoctf tux3000-picoctf  3771 Sep 25 16:29 .bashrc
-rw-r--r-- 1 tux3000-picoctf tux3000-picoctf   807 Sep 25 16:29 .profile
-rw-rw-r-- 1 tux3000-picoctf tux3000-picoctf   167 Sep 25 16:36 .wget-hsts
-rw-r--r-- 1 root            root             4443 Sep 25 16:35 README.txt
-rw-rw-r-- 1 tux3000-picoctf tux3000-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 tux3000-picoctf tux3000-picoctf 10936 Mar 16  2021 warm
tux3000-picoctf@webshell:~$ chmod +x warm 
tux3000-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
tux3000-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
tux3000-picoctf@webshell:~$
```
## Notas adicionales
## Referencias