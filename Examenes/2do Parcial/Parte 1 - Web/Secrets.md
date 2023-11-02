# Secrets
## Objetivo

We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:62050/).
## Solución

```shell

```

La bandera la encontré inspeccionado la pagina y revisando las fuentes de la aplicación, al parecer existía una carpeta llamada secret, entonces edite la ruta de la pagina con esta nueva ruta de la carpeta y de nuevo realice una inspección a la pagina, aquí encontré una carpeta llamada hidden, nuevamente edite la ruta de la pagina y final mente inspeccione la pagina y vi la carpeta superhidden, edite la ruta de la pagina y cuando hice una inspección en su estructura HTML se encontraba la bandera.

**Bandera:** picoCTF{succ3ss_@h3n1c@10n_51b260fe}
## Notas adicionales
## Referencias