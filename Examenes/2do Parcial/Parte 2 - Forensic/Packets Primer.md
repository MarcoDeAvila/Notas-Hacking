# Packets Primer
## Objetivo

Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/196/network-dump.flag.pcap)
## Solución

```shell

```

La solución la obtuve interceptando el archivo de comunicaciones y visualizando el paquete **#1** de la comunicación con protocolo **TCP**, hago un seguimiento de sus streams y el stream **#0** contenía la bandera.

**Bandera:** picoCTF{p4ck37_5h4rk_01b0a0d6}
## Notas adicionales
## Referencias