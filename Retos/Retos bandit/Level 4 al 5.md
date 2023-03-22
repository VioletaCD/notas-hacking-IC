# Bandit Level 4 → Level 5

## Objetivo

The password for the next level is stored in a hidden file in the **inhere** directory.

## Datos de acceso al nivel
- bandit4 
- 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
## Solucion
```
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: Non-ISO extended-ASCII text, with NEL line terminators
./-file06: Non-ISO extended-ASCII text, with no line terminators, with escape sequences
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$
```

## Notas adicionales
LA CONTRASEÑA DICE ESTAR EN EL ÚNICO ARCHIVO LEGIBLE POR HUMANOS EN EL DIRECTORIO **_INHERE_**. CLARO, NOSOTROS NOS ENCONTRAMOS CON 10 ARCHIVOS... LA GRAN MAYORÍA DE ELLOS MOSTRANDO INFORMACIÓN AL PARECER ENCRIPTADA O PROTEGIDA. BUENO PUES SI HICIÉRAMOS UN **_CAT_** GLOBAL (**_*_**) DE TODO LO QUE CONTIENE EL DIRECTORIO **_INHERE_**... POR ALGÚN LADO LOGRAREMOS VER LA CONTRASEÑA EN TEXTO PLANO, DADO QUE NO DEBERÍA DE ESTAR PROTEGIDA O ENCRIPTADA:

## Referencias
- https://mundo-hackers.weebly.com/bandit.html
- https://www.w0lff4ng.org/wargame-bandit-1/