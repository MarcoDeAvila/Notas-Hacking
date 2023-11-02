# SQL Direct
## Objetivo

Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
## Solución

```SQL
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# SELECT * FROM FLAGS;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# SELECT address FROM FLAGS WHERE id = 1;
                address                 
----------------------------------------
 picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
(1 row)
```

Me conecte al servidor PostgreSQL que menciona el reto y solo tuve que inspeccionar las tablas que tenia esta base de datos, realice unas consultas y obtuve la bandera.

**Bandera:** picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
## Notas adicionales
## Referencias

[PostgreSQL: Documentation: 8.3: psql](https://www.postgresql.org/docs/8.3/app-psql.html)