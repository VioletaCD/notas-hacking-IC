# Bandit Level 9 → Level 10

## Objetivo

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso al nivel
- bandit9
- EN632PlfYiZbn3PhVK3XOGSlNInNE00t
## Solucion
```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$  strings data.txt | grep ==
f========== theM
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
```

## Notas adicionales
   usamos el comando `strings`, quien nos imprime las cadenas de caracteres `imprimibles` en un archivo. El output de este comando lo redireccionamos a un `grep`, para buscar por varios `=`
## Referencias
- https://mundo-hackers.weebly.com/bandit.html
- https://www.w0lff4ng.org/wargame-bandit-1/