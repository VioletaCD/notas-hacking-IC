# SQL Direct
## Descripcipción
Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
## Pistas
- This challenge launches an instance on demand.  
Its current status is: `NOT_RUNNING`
## Solucion
```
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 52895 -U postgres pico
Password for user postgres: 
psql (15.2 (Debian 15.2-2))
Type "help" for help.

pico=# table flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 
```
## Bandera
picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=iK68Xr3sNPQ