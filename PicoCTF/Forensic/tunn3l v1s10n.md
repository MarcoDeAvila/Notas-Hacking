# tunn3l v1s10n
## Objetivo

We found this [file](https://mercury.picoctf.net/static/09a86202e72dbdb5bf4d1b5d2c6a5b86/tunn3l_v1s10n). Recover the flag.
## Solución

```shell

```

El archivo contenía binarios corrompidos que no encajaban en el tipo de archivo bmp, para ello edite el encabezado para poder abrir el archivo, se trataba de una imagen de alta calidad, además observado sus metadatos me di cuenta que tenia dimensiones extrañas para el tamaño limitado  de la imagen, entonces cambie estos binarios para hacer mas alta la imagen, guarde cambios y al abrir la imagen ahora si podía observar la bandera, se encontraba en la parte superior de la imagen.

**Bandera:** picoCTF{qu1t3_a_v13w_2020}
## Notas adicionales

|Formato| Descripción|
|-|-|
|bmp| El formato BMP es un archivo rasterizado sin comprimir diseñado para mostrar imágenes de alta calidad en Windows y almacenar fotos imprimibles.|
## Referencias