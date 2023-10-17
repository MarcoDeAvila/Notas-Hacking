# Shark On Wire 1
## Objetivo

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Solución

```shell

```

La solución la obtuve interceptando el archivo de comunicaciones y visualizando el paquete **#11** de la comunicación con protocolo **UDP**, hago un seguimiento de sus streams y el stream **#6** contenia la bandera. 

**Bandera:** picoCTF{StaT31355_636f6e6e}
## Notas adicionales

|Comando | Descripción |
|-|-|
|wireshark| Herramienta para capturar paquetes en la red.|
## Referencias

[Cómo capturar tráfico con Wireshark y analizarlo para detectar anomalías (redeszone.net)](https://www.redeszone.net/tutoriales/redes-cable/wireshark-capturar-analizar-trafico-red/)

