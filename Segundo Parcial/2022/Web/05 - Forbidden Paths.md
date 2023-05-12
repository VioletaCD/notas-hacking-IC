# Forbidden Paths
## Descripcipción
Can you get the flag? Here's the [website](http://saturn.picoctf.net:52278/). We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Pistas
- (None)
## Solucion
```
Para obtener la bandera:
el reto nos otorga una pagina web y un direccionamiento
en la pagina hay un espacio para hacer una busqueda
ahi se ingresa el direccionamiento con los siguientes cambios
/../../../flag.txt
```
## Bandera
picoCTF{7h3_p47h_70_5ucc355_6db46514}
## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=3PKop-SYmoE