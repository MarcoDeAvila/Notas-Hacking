# vault-door-5
## Objetivo

In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/d31ce4356bdfd15d33a9af7e35ab4d0a/VaultDoor5.java)
## Solución

```shell

```

Encontré la contraseña viendo el script que nos proporcionan y en su metodo 'checkPassword' se encontraba lo que parecía el mensaje que necesitaba descifrar, utilice cyberchef para ello, con herramientas de base64 y URL Decode para conseguirlo.

**Bandera:** picoCTF{c0nv3rt1ng_fr0m_ba5e_64_e3152bf4}
## Notas adicionales
## Referencias

[From Base64, URL Decode - CyberChef (gchq.github.io)](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)URL_Decode()&input=SlRZekpUTXdKVFpsSlRjMkpUTXpKVGN5SlRjMEpUTXhKVFpsSlRZM0pUVm1KVFkySlRjeUpUTXdKVFprSlRWbUpUWXlKVFl4SlRNMUpUWTFKVFZtSlRNMkpUTTBKVFZtSlRZMUpUTXpKVE14SlRNMUpUTXlKVFl5SlRZMkpUTTA)