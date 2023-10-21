# WhitePages
## Objetivo

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!
## Solución

```python
rom pwn import *

file = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)

```

Lo resolví cambiando los caracteres en blanco del codificador UNICODE UTF-8 por caracteres de 0 y 1, para obtener una cadena en código ASCII que esta incluía la bandera.

**Bandera:** picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}
## Notas adicionales

[Un recorrido rápido por Unicode—ArcGIS Pro | Documentación](https://pro.arcgis.com/es/pro-app/latest/help/data/geodatabases/overview/a-quick-tour-of-unicode.htm)
## Referencias