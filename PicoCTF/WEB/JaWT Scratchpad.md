# JaWT Scratchpad
## Objetivo

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210
## Solución

```shell
┌──(kali㉿kali)-[~]
└─$ nano jawt    
┌──(kali㉿kali)-[~]
└─$ cat jawt                                           
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiVHV4In0.y9YPTMX_2edRL4EeYxi8CT38Bh2FZGzKFthQU5sP3jw
┌──(kali㉿kali)-[~]
└─$ sudo gzip -d /usr/share/wordlists/rockyou.txt.gz 
┌──(kali㉿kali)-[~]
└─$ ls /usr/share/wordlists                            
amass      fasttrack.txt  legion      rockyou.txt  wifite.txt
dirb       fern-wifi      metasploit  sqlmap.txt
dirbuster  john.lst       nmap.lst    wfuzz
┌──(kali㉿kali)-[~]
└─$ head /usr/share/wordlists/rockyou.txt                
123456
12345
123456789
password
iloveyou
princess
1234567
rockyou
12345678
abc123
┌──(kali㉿kali)-[~]
└─$ john jawt --show
?:ilovepico

1 password hash cracked, 0 left
┌──(kali㉿kali)-[~]
└─$ 

```

De esta manera obtuve la palabra **ilovepico**, edite la cookie cambiando el nombre por 'admin' y crackeado la contraseña, obteniendo un nuevo valor para la cookie.

**Bandera:** picoCTF{jawt_was_just_what_you_thought_44c752f5}
## Notas adicionales

Resolví el reto 8hr después de lo marcado por la plataforma de picoCTF. 

|Herramienta| Descripcion|
|-|-|
|john|John the Ripper es una herramienta de crackeo de contraseñas|
## Referencias

[JSON Web Tokens - jwt.io](https://jwt.io/)
[PicoCTF: JaWT Scratchpad (Challenge 15) - YouTube](https://www.youtube.com/watch?v=AL8RIvQgbTg&t=406s)