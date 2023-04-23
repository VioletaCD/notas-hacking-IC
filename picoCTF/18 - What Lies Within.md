# What Lies Within
## Descripcipción
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
## Pistas
- There is data encoded somewhere... there might be an online decoder.
## Solucion
```
SOLUCIÓN 1
Usando una pagina web que nos permite decodificar lo que se encuentra dentro de la imagen

SOLUCIÓN 2
┌──(kali㉿kali)-[~/Documents/forense/What Lies Within]
└─$ zsteg -a buildings.png | grep picoCTF
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"

```
## Bandera
picoCTF{h1d1ng_1n_th3_b1t5}
## Notas adicionales
instalar zsteg, herramienta de ruby
## Referencias
https://es.wikipedia.org/wiki/Esteganograf%C3%ADa
https://www.youtube.com/watch?v=bFUB-USG3sw&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=18