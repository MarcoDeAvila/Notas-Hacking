# Convertme.py
## Objetivo

Run the Python script and convert the given number from decimal to binary to get the flag.
[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)
## Solución

```shell
tux3000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
tux3000-picoctf@webshell:~$ ls
README.txt  convertme.py
tux3000-picoctf@webshell:~$ python convertme.py 
If 36 is in decimal base, what is it in binary base?
Answer: 100100
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
tux3000-picoctf@webshell:~$ 

36 = 100100
```
## Notas adicionales

La respuesta correcta y solución al reto solo era convertir el numero 36 a binario.
## Referencias

[36 decimal to binary conversion (rapidtables.com)](https://www.rapidtables.com/convert/number/decimal-to-binary.html?x=36)