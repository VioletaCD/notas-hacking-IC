# Bandit Level 6 → Level 7

## Objetivo

The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

## Datos de acceso al nivel
- bandit6
- P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
## Solucion
```
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Feb 21 22:02 .
drwxr-xr-x 70 root root 4096 Feb 21 22:04 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```

## Notas adicionales
Esto ha sido mucho más óptimo. Dado que sabemos quién es el propietario del fichero y qué grupo está asignado a dicho archivo... Nuestra búsqueda se simplifica bastante. Recordad que el 2>/dev/null se pone para evitar mostrar mensajes de error por pantalla, dado que la búsqueda es profunda bajo toda la raíz... Y hay directorios a los que no se tiene permisos de acceso... Por lo que nos podrían salir mensajes del tipo "acceso denegado". Usando ese pequeño "truco" al final de nuestra sentencia de comandos, nos ahorramos los mensajes de error.
## Referencias
- https://mundo-hackers.weebly.com/bandit.html
- https://www.w0lff4ng.org/wargame-bandit-1/