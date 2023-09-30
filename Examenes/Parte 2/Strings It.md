# Strings It
## Objetivo

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?
## Solución

```shell
tux3000-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
tux3000-picoctf@webshell:~$ ls
README.txt  strings
tux3000-picoctf@webshell:~$ cat strings | grep picoCTF
grep: (standard input): binary file matches
tux3000-picoctf@webshell:~$ string strings | grep picoCTF
-bash: string: command not found
tux3000-picoctf@webshell:~$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_d66c7bb7}
tux3000-picoctf@webshell:~$ 
```
## Notas adicionales

|Comando |Descripción |
|-|-|
|strings| Muestra las cadenas de caracteres imprimibles que contengan los ficheros.|

Para encontrar la bandera fue necesario usar le comando "strings" en conjunto con el comando "grep" para filtrar la búsqueda.
## Referencias