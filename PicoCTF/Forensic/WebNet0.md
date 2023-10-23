# WebNet0
## Objetivo

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solución

```shell

```

interceptando la comunicación del archivo de paquetes puede observar el protocolo TLS pero por el momento no era posible darles seguimiento, entonces lo único que hice fue añadir la llave proporcionada para poder desencriptar estos paquetes, con la llave puesta puede darles seguimiento y ahí encontré la bandera.

**Bandera:** picoCTF{nongshim.shrimp.crackers}
## Notas adicionales
## Referencias