# MacroHard WeakEdge
## Objetivo

I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/3944a59474f9f676942282c50b9c3675/Forensics%20is%20fun.pptm)
## Solución

```shell
┌──(kali㉿kali)-[~/picoCTF/Forensic]
└─$ echo 'Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q' | tr -d " "
ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ
                                                                                                                      
┌──(kali㉿kali)-[~/picoCTF/Forensic]
└─$ echo 'Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q' | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
                                                                                                                      
┌──(kali㉿kali)-[~/picoCTF/Forensic]
└─$ 
```

La solución la obtuve desempaquetando el archivo proporcionado y luego navegue por las carpetas y encontré el archivo llamada 'Hidden' que tenia una cadena de caracteres en base64, solo tuve que decodificar esta cadena.

**Bandera:** picoCTF{D1d_u_kn0w_ppts_r_z1p5}
## Notas adicionales


## Referencias