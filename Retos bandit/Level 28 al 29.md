# Bandit Level 26 → Level 27

## Objetivo

Hay un repositorio de git en `ssh://bandit28-git@localhost/home/bandit28-git/repo`. La contraseña para el usuario `bandit28-git`es la misma que para el usuario `bandit28`.

Clona el repositorio y encuentra la contraseña para el siguiente nivel.

Clona el repositorio y encuentra la contraseña para el siguiente nivel.
## Datos de acceso al nivel
- bandit28 
- AVanL161y9rsbcJIsFHuw35rjaOM19n
## Solucion
````
bandit28@bandit:~$ mkdir /tmp/repo1337
bandit28@bandit:~$ cd /tmp/repo1337
bandit28@bandit:/tmp/repo1337$ git clone ssh://bandit28-git@localhost/home/bandit28-git/repo
Cloning into 'repo'...
bandit28-git@localhost password: 

remote: Counting objects: 9, done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0)
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (2/2), done.
bandit28@bandit:/tmp/repo1337$ ls
repo
bandit28@bandit:/tmp/repo1337$ cd repo/
bandit28@bandit:/tmp/repo1337/repo$ ls
README.md
bandit28@bandit:/tmp/repo1337/repo$ cat README.md 
# Bandit Notes
Some notes for level29 of bandit.
`````

## Notas adicionales
debe crear una carpeta temporal en **/tmp/** y clonar el repositorio. Luego, para revelar la contraseña, debe verificar una confirmación anterior.
## Referencias
- https://mayadevbe.me/posts/overthewire/bandit/level28/
- https://medium.com/secttp/overthewire-bandit-level-28-2a5453c6e76c