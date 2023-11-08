# Mind your Ps and Qs
## Objetivo

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values)
## Solución

```shell
tux3000-picoctf@webshell:~$ cat values 
Decrypt my super sick RSA:
c: 843044897663847841476319711639772861390329326681532977209935413827620909782846667
n: 1422450808944701344261903748621562998784243662042303391362692043823716783771691667
e: 65537tux3000-picoctf@webshell:~$ python
```
``` python
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> 
>>> c = 843044897663847841476319711639772861390329326681532977209935413827620909782846667
>>> e = 65537
>>> p = 2159947535959146091116171018558446546179
>>> q = 658558036833541874645521278345168572231473
>>> 
>>> n = p * q
>>> tn = (p-1)*(q-1)
>>> d = inverse(e, tn)
>>> m = pow(c,d,n)
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_00264570}'
>>
```

Los valores de p y q que los obtuve factorizando el valor de n, con estos nuevos valores solo aplique las operaciones para encontrar la bandera.

**Bandera:** picoCTF{sma11_N_n0_g0od_00264570}
## Notas adicionales
## Referencias

[factordb.com](http://factordb.com/index.php?query=1422450808944701344261903748621562998784243662042303391362692043823716783771691667)