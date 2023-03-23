# Scavenger Hunt
## Descripcipción
There is some interesting information hidden around this site [http://mercury.picoctf.net:44070/](http://mercury.picoctf.net:44070/). Can you find it?
## Pistas
- You should have enough hints to find the files, don't run a brute forcer.
## Solucion
```
- se visita el sitio dado por el reto
- se visita el codigo fuente de la pagina, encontrando ahi la primera parte de la bandera.
- se visita la liga del css del codigo web y encontramos ahi la segunda parte de la bandera.
- se visita el myjs y encontramos el siguiente texto "How can I keep Google from indexing my website?"
- Esto nos lleva a implementar el metodo robots en el link y asi encontrar la ultima parte de la bandera.
```
## Bandera
picoCTF{th4ts_4_l0t_0f_pl4c}
## Notas adicionales
## Referencias

