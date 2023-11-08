# basic-mod1
## Objetivo

We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/128/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución

```shell

```

Me ayude de una pagina web que descifra este tipo de mensajes en módulos, solo tuve que aplicar el formato de las banderas de pico.

**Bandera:** picoCTF{r0und_n_r0und_b6b25531}
## Notas adicionales

|Concepto| Descripción|
|-|-|
|Cifrado Modulo | Un cifrado módulo utiliza cálculo modular en números para extraer el resto. Los valores obtenidos se pueden utilizar como código/índice para otro cifrado, como A1Z26 o el código ASCII.|
## Referencias

[Modulo Cipher (26, 27, 36, 37, 128) - Decodificador/Codificador en línea (dcode.fr)](https://www.dcode.fr/modulo-cipher)