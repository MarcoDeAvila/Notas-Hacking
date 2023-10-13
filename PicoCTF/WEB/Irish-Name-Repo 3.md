# Irish-Name-Repo 3
## Objetivo
## Solución

```shell

```

Entre a la pagina y para este reto no teníamos campo para el usuario, simplemente teníamos que entrar con la contraseña para admin, en general las contraseñas son encriptadas y por ende al intentar hacer un SQL injection **' or 1=1;** este valor cambiaba y no se reconocía como una sentencia validad para SQL, fue sencillo analizar este comportamiento y lo único que hice fue inyectar un SQL injection encriptado a rot13 de **'be 1=1;**. 

**Bandera:** picoCTF{3v3n_m0r3_SQL_4424e7af}
## Notas adicionales
## Referencias

[CyberChef (gchq.github.io)](https://gchq.github.io/CyberChef/)

