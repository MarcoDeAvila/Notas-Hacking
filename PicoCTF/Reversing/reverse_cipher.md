# reverse_cipher
## Objetivo

We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this). Can you reverse the flag.
## Solución

``` shell
tux3000-picoctf@webshell:~$ nano bandera.py 
tux3000-picoctf@webshell:~$ python bandera.py 
picoCTF{w1{1wq84fb<1>49}
r3v3rs36ad73964
```
```python
cifrado = open('rev_this','r').read()  
print(cifrado)  
  
flag = ''  
  
for i in range(8, len(cifrado)-1):  
       if i & 1 == 0:  
               flag +=chr(ord(cifrado[i])-5)  
       else:  
               flag += chr(ord(cifrado[i])+2)  
  
print(flag)
```

**Bandera:** picoCTF{r3v3rs36ad73964}
## Notas adicionales
## Referencias