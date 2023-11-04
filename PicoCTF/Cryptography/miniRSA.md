# miniRSA
## Objetivo

Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/ee7e2388b45f521b285334abb5a63771/ciphertext)? Something seems a bit small.
## Solución

```python
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from gmpy2 import *
>>> from Crypto.Util.number import long_to_bytes
>>> gmpy2.get_context().precision = 2048
>>> e = 3
>>> c = 2205316413931134031074603746928247799030155221252519872649649212867614751848436763801274360463406171277838056821437115883619169702963504606017565783537203207707757768473109845162808575425972525116337319108047893250549462147185741761825125
>>> root, exact = iroot(c, e)
>>> root
mpz(13016382529449106065894479374027604750406953699090365388202874238148389207291005)
>>> print( long_to_bytes(root))
b'picoCTF{n33d_a_lArg3r_e_606ce004}'
>>> 
```

Se aplico el algoritmo rsa al archivo en python para llegar a la bandera.

**Bandera:** picoCTF{n33d_a_lArg3r_e_606ce004}
## Notas adicionales
## Referencias