# GET aHEAD
## Descripcipción
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:21939/](http://mercury.picoctf.net:21939/)
## Pistas
- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses
## Solucion
```
-- RESPUESTA DESDE NAVEGAD
- se visita el codigo fuente de la pagina
- se usa el inspector
- se selecciono la pestaña de red
- se renvio el head y otorgó la bandera

picoCTF{r3j3ct_th3_du4l1ty_6ef27873}

--RESPUESTA DESDE TERMINAL
┌──(kali㉿kali)-[~]
└─$ curl -I http://mercury.picoctf.net:21939/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_6ef27873}
Content-type: text/html; charset=UTF-8

```
## Bandera
picoCTF{r3j3ct_th3_du4l1ty_6ef27873}
## Notas adicionales
El usuario ingresa datos y altera la entrada
## Referencias
https://www.w3schools.com/sql/sql_injection.asp
