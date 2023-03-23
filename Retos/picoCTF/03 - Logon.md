#  Logon
## Descripcipción
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/13594/` ([link](https://jupiter.challenges.picoctf.org/problem/13594/)) or http://jupiter.challenges.picoctf.org:13594
## Pistas
- Hmm it doesn't seem to check anyone's password, except for Joe's?
## Solucion
```
instalar cookieeditor

-se ingresa con jobs
-se ingresa otro username y password
-se modifica la cookie admin
	poniendola en True
	se refresca el sitio 
-Muestra la bandera

`picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}`
```
## Bandera
picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}
## Notas adicionales
## Referencias
