# m00nwalk
## Objetivo

Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.
## Solución

```

```

La solucion a este reto la encontre investigando lo que me trataban de decir las pistas, encontré que se enviaron las imágenes de la tierra mediante audios en un formato **SSTV**, entonces encontré una herramienta que me permitiera cambiar el formato wav a png, dentro de la imagen estaba la bandera.

**Bandera:** picoCTF{beep_boop_im_in_space}
## Notas adicionales

|Herramienta| Descripcion|
|-|-|
|ssvt| decodificación de imágenes SSTV |
## Referencias

[colaclanth/sstv: Decodificador SSTV (github.com)](https://github.com/colaclanth/sstv)
[Cómo recibir imágenes SSTV – Radio Club de Concepción CE5JA](https://www.ce5ja.cl/como-recibir-imagenes-sstv/#:~:text=Esta%20t%C3%A9cnica%20se%20conoce%20como,Android%20utilizando%20la%20aplicaci%C3%B3n%20Robot36.)