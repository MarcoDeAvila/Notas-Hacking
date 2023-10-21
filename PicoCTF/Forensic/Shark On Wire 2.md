# Shark On Wire 2
## Objetivo

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
## Solución

```python
from scapy.all import *
packets = rdpcap('capture.pcap.1')
flag = ''
for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)
```

La solución la obtuve interceptando el archivo de comunicaciones y visualizando el paquete **#11** de la comunicación con protocolo **UDP**, hago un seguimiento de sus streams y el stream **#32** indica el comienzo y el stream **#60** indica la finalización de la bandera en el puerto 5000, pero no era fue tan sencillo descifrarla debido a que se encontraba codificados y tuve que obtener esos caracteres.

**Bandera:** picoCTF{p1LLf3r3d_data_v1a_st3g0}
## Notas adicionales
## Referencias