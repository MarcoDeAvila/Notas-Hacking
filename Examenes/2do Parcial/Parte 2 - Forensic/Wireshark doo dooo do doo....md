# Wireshark doo dooo do doo...
## Objetivo

Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/0505a462ac9beb7412596855df280f6b/shark1.pcapng).
## Solución

```shell

```

La solución la obtuve interceptando el archivo de comunicaciones y visualizando el paquete **#2** de la comunicación con protocolo **HTTP**, hago un seguimiento de sus streams y el stream **#5** contenía lo que parecía la bandera, pero se encontraba en con un formato al parecer de rot13, use ciberchef para dar con la bandera.

**Bandera:** picoCTF{p33kab00_1_s33_u_deadbeef}
## Notas adicionales
## Referencias

[ROT13 - CyberChef (gchq.github.io)](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=Y3ZwYlBHU3tjMzN4bm8wMF8xX2YzM19oX3FybnFvcnJzfQ)