# Enhance!
## Objetivo

Download this image file and find the flag.

- [Download image file](https://artifacts.picoctf.net/c/101/drawing.flag.svg)
## Solución

```shell
┌──(kali㉿kali)-[~/picoCTF/Forensic]
└─$ cat drawing.flag.svg | grep tspan
       id="text3723"><tspan
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ 2 4 3 7 4 6 7 5 }</tspan></text>
                                                                                                  
┌──(kali㉿kali)-[~/picoCTF/Forensic]
└─$
```

Revise el archivo mostrando su contenido en pantalla, observé que el identificador "tspan" mostraba lo que parecia ser parte de la estructura de la bandera, entonces solo filtre esta impresión de contenido por el id mencionado y obtuve la bandera. 

**Bandera:** picoCTF{3nh4nc3d_24374675}
## Notas adicionales
## Referencias