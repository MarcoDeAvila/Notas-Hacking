# c0rrupt
## Objetivo

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Solución

```shell

```

Para este reto lo primero que intente hacer fue reconocer el tipo de archivo de cual se trataba el que nos proporcionaban, algunos bites correspondían a un tipo de imagen png el cual esta corrompido por varios métodos.

1 - El tipo de archivo.
2 - Especificación de chunks de png.

Para resolverlo tuve que usar un editor hexadecimal para editar sus binarios y dar el formato adecuado al archivo.

Por otro lado tuve que instalar una herramienta que me permite checar los archivos png, esta herramienta me brinda la información necesaria para dar solución a aquellos chunks que encontraba dañados, al final cambiar algunos bits de los chunks resolvió el archivo corrompido y pude ver la bandera especificada en la imagen png.

**Bandera:** picoCTF{c0rrupt10n_1847995}
## Notas adicionales

|Herramienta| Descripcion|
|-|-|
|pngcheck| verifica la integridad de los archivos PNG, JNG y MNG|
## Referencias

[Convertidor de texto a hexadecimal en línea (magictool.ai)](https://magictool.ai/tool/text-to-hex-converter/es/)
[PNG Specification: Chunk Specifications (libpng.org)](http://www.libpng.org/pub/png/spec/1.2/PNG-Chunks.html)