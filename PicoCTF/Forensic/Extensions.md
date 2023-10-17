# Extensions
## Objetivo

This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Solución

```shell

```

La solución de este reto estaba en el archivo .txt que proporciona la pagina, pero al analizar el archivo me di cuenta que no se trataba de un archivo de texto convencional, resulta ser que este archivo en realidad era un archivo png, entonces para encontrar la solución solo cambie la extensión y visualicé el nuevo archivo, la bardera en realidad estaba en la imagen.

**Bandera:** picoCTF{now_you_know_about_extensions}
## Notas adicionales

Existen bites de un archivo que indican el tipo de archivo correcto, son conocidos como firmas para los archivos y están estandarizados, también es posible encontrarlos como **magic bites**.

Era posible saber que el archivo del reto no era un txt observando los bites.
## Referencias

[Magic Bytes – Identifying Common File Formats at a Glance (netspi.com)](https://www.netspi.com/blog/technical/web-application-penetration-testing/magic-bytes-identifying-common-file-formats-at-a-glance/)