# Bandit Level 10 → Level 11

## Objetivo

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de acceso al nivel
- bandit10
- G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
## Solucion
```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "hola mundo"
hola mundo
bandit10@bandit:~$ echo "hola mundo" | base64
aG9sYSBtdW5kbwo=
bandit10@bandit:~$  echo -n aG9sYSBtdW5kbwo= | base64 -d
hola mundo
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```

## Notas adicionales
  Como se indicó en las instrucciones, el contenido del archivo es un string en [base64](https://en.wikipedia.org/wiki/Base64). Para estos casos, Linux posee una herramienta para codificar y decodificar la base mencionada.

Si revisamos el manual del comando `base64`, vemos que tiene una opción `-d`, que permite decodificar datos
## Referencias
- https://mundo-hackers.weebly.com/bandit.html
- https://www.w0lff4ng.org/wargame-bandit-1/