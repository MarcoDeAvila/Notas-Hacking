# WebNet1
## Objetivo

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución

```shell

```

interceptando la comunicación del archivo de paquetes puede observar el protocolo TLS pero estos no tenían la bandera aquí, entonces lo único que hice fue añadir la llave proporcionada para poder desencriptar estos paquetes, con la llave puesta encontré que se estaba bajando un paquete, se trataba de una imagen, la exporte y luego revise los strings de esta, aquí encontré la bandera.

**Bandera:** picoCTF{honey.roasted.peanuts}
## Notas adicionales
## Referencias