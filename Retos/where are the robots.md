#  where are the robots
## Descripcipción
Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/41511/` ([link](https://jupiter.challenges.picoctf.org/problem/41511/)) or http://jupiter.challenges.picoctf.org:41511
## Pistas
- How do you inspect web code on a browser?
- There's 3 parts
## Solucion
```
- se ingresó a la pagina dada por el reto:
- el robots.txt en el fin del link dado
- se encontró lo siguiente:
Agente de usuario: *
No permitir: /477ce.html
-se agrego a la ultima parte del link:
/477ce.html
y en ese sitio se encontró la bandera.

Supongo que encontraste los robots.  
picoCTF{ca1cu1at1ng_Mach1n3s_477ce}
```
## Bandera
picoCTF{ca1cu1at1ng_Mach1n3s_477ce}
## Notas adicionales
## Referencias
