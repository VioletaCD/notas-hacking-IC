# Bandit Level 2 → Level 3

## Objetivo

The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso al nivel
bandit2
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
## Solucion
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

## Notas adicionales
cuando hay espacios en el nombre hay que delimitarlo

## Referencias
https://mundo-hackers.weebly.com/bandit.html