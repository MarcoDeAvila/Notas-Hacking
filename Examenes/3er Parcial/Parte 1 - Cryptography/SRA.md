# SRA
## Objetivo

I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...

Additional details will be available after launching your challenge instance.
## Solución

```shell
tux3000-picoctf@webshell:~$ python exp.py 
[+] Opening connection to saturn.picoctf.net on port 50740: Done
/home/tux3000-picoctf/exp.py:26: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("anger =")
/home/tux3000-picoctf/exp.py:29: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("envy =")
cipher= 46040414026875221996389700403860393025329039125983090645873376265924481567484
d= 47473134178694758856022933239224814555863250009745888671049164983240927727777
/home/tux3000-picoctf/exp.py:33: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("vainglory?"))
b'vainglory?'
Give me the divisors of  3111246794669118411147174975699076671547609815888716305834549125506660680495321248
[2, 2, 2, 2, 2, 3, 3, 3, 7, 7, 113, 179, 725506394911, 2205181503692117, 45304232350136288314393, 50126664072595947030599]
{199808110434981183802907539463943479963, 231920208581950987359867987376240386289, 273408724927802759347846225537720537903, 171071380960412899703680319889523465057}
Lj5o80QSLmBPQdzA
/home/tux3000-picoctf/exp.py:61: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendline(plaintext.decode())
b'> Lj5o80QSLmBPQdzA\r\n'
b'Conquered!\r\n'
b'picoCTF{7h053_51n5_4r3_n0_m0r3_2b7ad1ae}\r\n'
Lj5o80QSLmBPQdzA
[*] Closed connection to saturn.picoctf.net port 50740
tux3000-picoctf@webshell:~$ 
```

```python
from pwn import *
import primefac
from itertools import combinations
from Crypto.Util.number import long_to_bytes

#function to generate all the sub lists
def sub_lists (l):
   # initializing empty list
    comb = []

    #Iterating till length of list
    for i in range(1,len(l)+1):
       # Generating sub list
        comb += [list(j) for j in combinations(l, i)]
   # Returning list
    return comb

def divisors(phi):
   print("Give me the divisors of ", phi-1)
  # this is dangerous, but I'm trusting me
   return(eval(input()))

#connect to the server
r = remote('saturn.picoctf.net', 62417)
#get ciphertext
r.recvuntil("anger =")
ciphertext=int(r.recvline())
#get d
r.recvuntil("envy =")
d=int(r.recvline())
print("cipher=",ciphertext)
print("d=",d)
print(r.recvuntil("vainglory?"))
r.recvline()
#since d is e^-1 mod (p-1)*(q-1), d*e=k*(p-1)*(q-1)+1
#so (p-1)*(q-1)*k = d*e-1
factors=divisors(d*65537)
combos = sub_lists(factors)
primes = set()
#try all possible subsets of the list of factors as the factors of (p-1)
for l in combos:
   product = 1
  # multiply them together to get p-1
   for k in l:
      product = product * k
  # if the right length and adding 1 yields a prime, then maybe
   if product.bit_length()==128 and primefac.isprime(product+1):
      primes.add(product+1)
print(primes)
primelist = list(primes)
#try all possible prime pairs
for p in primelist:
   for q in primelist:
      n=p*q
     # decode with this possible n
      plain = pow(ciphertext,d,n)
      try:
         plaintext = long_to_bytes(plain)
        # see if it corresponds to text and if so, try it
         print(plaintext.decode())
         r.sendline(plaintext.decode())
         print(r.recvline())
         print(r.recvline())
         print(r.recvline())
      except:
         continue
```

Utilice este script para dar con la bandera y use una herramienta web para obtener los divisores.

**Bandera:** picoCTF{7h053_51n5_4r3_n0_m0r3_2b7ad1ae}
## Notas adicionales

El script lo encontré navegando por en internet.
## Referencias

[Prime Factors Decomposition - Online Factorization Calculator (dcode.fr)](https://www.dcode.fr/prime-factors-decomposition)