# Bandit Level 17 → Level 18

## Objetivo

Hay 2 archivos en el directorio de inicio: **passwords.old y passwords.new** . La contraseña para el siguiente nivel está en **passwords.new** y es la única línea que se ha cambiado entre **passwords.old y passwords.new**

**NOTA: si ha resuelto este nivel y ve '¡Adiós!' al intentar iniciar sesión en bandit18, esto está relacionado con el siguiente nivel, bandit19**
## Datos de acceso al nivel
- bandit17 
- {llave privada} 
- VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
## Solucion
```
bandit17@bandit:~$ bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r-----  1 bandit17 bandit17   33 Feb 21 22:02 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .ssh
bandit17@bandit:~$ wc passwords.old
 100  100 3300 passwords.old
bandit17@bandit:~$ diff password.old passwords.new
diff: password.old: No such file or directory
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$ diff passwords.old passwords.new --color
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```

## Notas adicionales
Hay algunas formas de encontrar la contraseña para este nivel. Uno de los comandos no mencionados hace que el trabajo de este nivel sea realmente ligero, así que seguiremos con eso. Recuerde siempre, hay más de una forma de despellejar a un gato, especialmente con Linux.
## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/

