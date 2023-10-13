# Irish-Name-Repo 1
## Objetivo

There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
## Solución

```shell

```

Me dirigí al apartado de login de la pagina y utilice un SQL injection **'OR 1 = 1;'** en el campo del nombre y utilice cualquier palabra como contraseña para poder loguearme, en seguida obtuve acceso y encontré la bandera.

**Bandera:** picoCTF{s0m3_SQL_fb3fe2ad}
## Notas adicionales
## Referencias

[What is SQL Injection? Tutorial & Examples | Web Security Academy (portswigger.net)](https://portswigger.net/web-security/sql-injection)