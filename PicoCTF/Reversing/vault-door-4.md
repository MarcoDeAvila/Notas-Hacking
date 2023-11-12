# vault-door-4
## Objetivo

This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/c695ee23309d453a3ef369c34cc1bccb/VaultDoor4.java)
## Solución

```js
String.fromCharCode(106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 070 , 0146) + '4a6cbf3b';
'jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b'
```

Solo tuve que decodificar los caracteres, para ello realice utilice una función de JavaScript, una vez obtenido la bandera solo la comprobé ejecutando el archivo vaultdoor que se me proporciona.

**Bandera:** picoCTF{jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b}
## Notas adicionales
## Referencias