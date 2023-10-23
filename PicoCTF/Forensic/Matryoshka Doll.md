# Matryoshka Doll
## Objetivo

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/205adad23bf9d8303081a0e71c9beab8/dolls.jpg)
## Solución

```shell

```

La solución la obtuve sabiendo que dentro de la imagen que nos proporcionan existía un archivo oculto, para poder ver ese archivo utilice una herramienta para buscar archivos incrustados en una imagen binaria determinada y código ejecutable. Conociendo como funcionan las muñecas Matryoshka deduje que dentro del nuevo archivo encontrado existía uno oculto, entonces así fue, utilice la herramienta una y otra ves hasta encontrar la bandera.

**Bandera:** picoCTF{96fac089316e094d41ea046900197662} 
## Notas adicionales

|Herramienta | Descripcion|
|-|-|
|binwalk | Está diseñado para la identificación de archivos y el código incrustado dentro de las imágenes de firmware.|
## Referencias

[Paseo de basura | Herramientas de Kali Linux](https://www.kali.org/tools/binwalk/)