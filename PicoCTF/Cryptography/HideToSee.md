# HideToSee
## Objetivo

How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/240/atbash.jpg).
## Solución

```shell
┌──(kali㉿kali)-[~/picoCTF/Cryptography]
└─$ steghide extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                                                               
┌──(kali㉿kali)-[~/picoCTF/Cryptography]
└─$ ls
atbash.jpg  ciphertext  ciphertext.1  encrypted.txt  table.txt  the_numbers.png
                                                                                               
┌──(kali㉿kali)-[~/picoCTF/Cryptography]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_xz00558y}
```

Extraje los datos de la imagen con la herramienta steghide que me permite conocer los datos encriptados por estenografía, los datos que obtuve se guardaron en un archivo txt, al revisar este archivo tenia la bandera pero encriptada con atbash cipher, use cyberchef para conocer la bandera correcta.

**Bandera:** picoCTF{atbash_crack_ca00558b}
## Notas adicionales
## Referencias

[Esteganografía con Steghide: Guía completa de uso » EsGeeks](https://esgeeks.com/steghide-guia-de-uso/#google_vignette)
[Atbash Cipher - CyberChef (gchq.github.io)](https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfeHowMDU1OHl9)