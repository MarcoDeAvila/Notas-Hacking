# Caesar
## Objetivo

Decrypt this [message](https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext).
## Solución

```shell
┌──(kali㉿kali)-[~/picoCTF/Cryptography]
└─$ cat ciphertext 
picoCTF{ynkooejcpdanqxeykjrbdofgkq}
```

**Bandera:** picoCTF{crossingtherubiconvfhsjkou}
## Notas adicionales

En esta ocasión el mensaje no estaba encriptado con una rotación de 13 si no mas bien de 30.
## Referencias

[ROT13 - CyberChef (gchq.github.io)](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,30)&input=eW5rb29lamNwZGFucXhleWtqcmJkb2Zna3E)