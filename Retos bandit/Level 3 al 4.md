# Bandit Level 3 → Level 4

## Objetivo

The password for the next level is stored in a hidden file in the **inhere** directory.

## Datos de acceso al nivel
- bandit3 
- aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
## Solucion
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Feb 21 22:03 .
drwxr-xr-x 3 root    root    4096 Feb 21 22:03 ..
-rw-r----- 1 bandit4 bandit3   33 Feb 21 22:03 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```

## Notas adicionales
YA ESO DE OCULTO NOS LLAMA LA ATENCIÓN, PUES NOS VIENE A LA CABEZA EL PARÁMETRO '**_-A_**' DEL COMANDO _LS

## Referencias
- https://mundo-hackers.weebly.com/bandit.html
- https://man7.org/linux/man-pages/man1/ls.1.html
- https://man7.org/linux/man-pages/man1/cd.1p.html
- https://man7.org/linux/man-pages/man1/cat.1.html
- https://man7.org/linux/man-pages/man1/file.1.html
- https://man7.org/linux/man-pages/man1/du.1.html
- https://man7.org/linux/man-pages/man1/find.1.html