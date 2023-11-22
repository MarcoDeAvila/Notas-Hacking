# ASCII FTW
## Objetivo

This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/508/asciiftw).
## Solución

```java
void main(void)

{
  long lVar1;
  long in_FS_OFFSET;
  
  lVar1 = *(long *)(in_FS_OFFSET + 0x28);
  printf("The flag starts with %x\n",0x70);
  if (lVar1 != *(long *)(in_FS_OFFSET + 0x28)) {
    __stack_chk_fail();
  }
  return;
}
```

```
        00101184 c6 45 d0 70     MOV        byte ptr [RBP + -0x30],0x70
        00101188 c6 45 d1 69     MOV        byte ptr [RBP + -0x2f],0x69
        0010118c c6 45 d2 63     MOV        byte ptr [RBP + -0x2e],0x63
        00101190 c6 45 d3 6f     MOV        byte ptr [RBP + -0x2d],0x6f
        00101194 c6 45 d4 43     MOV        byte ptr [RBP + -0x2c],0x43
        00101198 c6 45 d5 54     MOV        byte ptr [RBP + -0x2b],0x54
        0010119c c6 45 d6 46     MOV        byte ptr [RBP + -0x2a],0x46
        001011a0 c6 45 d7 7b     MOV        byte ptr [RBP + -0x29],0x7b
        001011a4 c6 45 d8 41     MOV        byte ptr [RBP + -0x28],0x41
        001011a8 c6 45 d9 53     MOV        byte ptr [RBP + -0x27],0x53
        001011ac c6 45 da 43     MOV        byte ptr [RBP + -0x26],0x43
        001011b0 c6 45 db 49     MOV        byte ptr [RBP + -0x25],0x49
        001011b4 c6 45 dc 49     MOV        byte ptr [RBP + -0x24],0x49
        001011b8 c6 45 dd 5f     MOV        byte ptr [RBP + -0x23],0x5f
        001011bc c6 45 de 49     MOV        byte ptr [RBP + -0x22],0x49
        001011c0 c6 45 df 53     MOV        byte ptr [RBP + -0x21],0x53
        001011c4 c6 45 e0 5f     MOV        byte ptr [RBP + -0x20],0x5f
        001011c8 c6 45 e1 45     MOV        byte ptr [RBP + -0x1f],0x45
        001011cc c6 45 e2 41     MOV        byte ptr [RBP + -0x1e],0x41
        001011d0 c6 45 e3 53     MOV        byte ptr [RBP + -0x1d],0x53
        001011d4 c6 45 e4 59     MOV        byte ptr [RBP + -0x1c],0x59
        001011d8 c6 45 e5 5f     MOV        byte ptr [RBP + -0x1b],0x5f
        001011dc c6 45 e6 38     MOV        byte ptr [RBP + -0x1a],0x38
        001011e0 c6 45 e7 39     MOV        byte ptr [RBP + -0x19],0x39
        001011e4 c6 45 e8 36     MOV        byte ptr [RBP + -0x18],0x36
        001011e8 c6 45 e9 30     MOV        byte ptr [RBP + -0x17],0x30
        001011ec c6 45 ea 46     MOV        byte ptr [RBP + -0x16],0x46
        001011f0 c6 45 eb 30     MOV        byte ptr [RBP + -0x15],0x30
        001011f4 c6 45 ec 41     MOV        byte ptr [RBP + -0x14],0x41
        001011f8 c6 45 ed 46     MOV        byte ptr [RBP + -0x13],0x46
        001011fc c6 45 ee 7d     MOV        byte ptr [RBP + -0x12],0x7d

```

Caracteres ASCCI: 7069636f4354467b41534349495f49535f454153595f38393630463041467d

Lo primero que hice fue analizar el archivo con ghidra, con las herramientas que ofrece encontré la función main, desensamble esta función y encontré la pista **"The flag starts with %x\n",0x70"** que me indicaba que esta funcion tenia los caracteres ASCII que pertenecían a la bandera, comenzando con 70, entonces solo utilice una herramienta web para la traducción de estos.

**Bandera:** picoCTF{ASCII_IS_EASY_8960F0AF}
## Notas adicionales
## Referencias

[Hex to ASCII Text String Converter (rapidtables.com)](https://www.rapidtables.com/convert/number/hex-to-ascii.html)