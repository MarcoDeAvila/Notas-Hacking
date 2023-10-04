# Picobrowser
## Objetivo

This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/50522/` ([link](https://jupiter.challenges.picoctf.org/problem/50522/)) or http://jupiter.challenges.picoctf.org:50522
## Solución

```shell
tux3000-picoctf@webshell:~$ curl https://jupiter.challenges.picoctf.org/problem/50522/flag -H "User-Agent: picobrowser" | grep picoCTF
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  2115  100  2115    0     0   5548      0 --:--:-- --:--:-- --:--:--  5551
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_51414fa7}</code></p>
tux3000-picoctf@webshell:~$ 

```
**Bandera:** picoCTF{p1c0_s3cr3t_ag3nt_51414fa7}
## Notas adicionales
## Referencias