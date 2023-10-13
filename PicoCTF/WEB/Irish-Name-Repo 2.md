# Irish-Name-Repo 2
## Objetivo

There is a website running at `https://jupiter.challenges.picoctf.org/problem/53751/` ([link](https://jupiter.challenges.picoctf.org/problem/53751/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:53751
## Solución

```shell

```

Entre a la pagina y en esta ocasión con la SQL injection del reto anterior la pagina me detectaba este tipo de vulnerabilidad, sim embargó edite mi injection de la siguiente manera **admin';** para el campo de usuario y cualquier palabra para la contraseña, de esta manera esta omitiendo parte de la sentencia del login.

**Bandera:** picoCTF{m0R3_SQL_plz_c34df170} 
## Notas adicionales
## Referencias