# Tab, Tab, Attack
## Objetivo

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/e38f6a5b69b45d21e33cf7281d8c2531/Addadshashanammu.zip)
## Solución

```shell
tux3000-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/e38f6a5b69b45d21e33cf7281d8c2531/Addadshashanammu.zip
2023-09-25 17:25:25 (64.3 MB/s) - 'Addadshashanammu.zip' saved [4521/4521]
tux3000-picoctf@webshell:~$ ls -l
total 16
-rw-rw-r-- 1 tux3000-picoctf tux3000-picoctf 4521 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root            root            4443 Sep 25 17:23 README.txt
tux3000-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
tux3000-picoctf@webshell:~$ ls -l
total 16
drwxr-xr-x 3 tux3000-picoctf tux3000-picoctf   28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 tux3000-picoctf tux3000-picoctf 4521 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root            root            4443 Sep 25 17:23 README.txt
tux3000-picoctf@webshell:~$ ./Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_f3553887}
tux3000-picoctf@webshell:~$ 
```
## Notas adicionales

Se resolvió desempaquetando el archivo zip y ejecutando el archivo que se encontraba dentro de varios directorios.
## Referencias