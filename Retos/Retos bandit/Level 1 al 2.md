## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de acceso al nivel
- bandit1
- NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
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
NO CONSEGUIMOS VISUALIZAR NADA, SE QUEDA PILLADO (EL **_HOLA_** LO HE ESCRITO YO). Y ES INTERESANTE... PUES REALMENTE SE TRATA DE UN FICHERO Y AHÍ DENTRO ESTÁ LA CONTRASEÑA EN FORMATO HASH PARA ACCEDER A **_BANDIT2_**.  
  
EL PROBLEMA ESTÁ EN EL NOMBRE DEL FICHERO -> '**_-_**', A ESTE TIPO DE FICHEROS SE LES LLAMA **_FICHEROS O ARCHIVOS DE NOMBRE DISCONTINUOS_** (**_DASH FILE_**). EL INCONVENIENTE SURGE CUANDO TRATAMOS DE USAR **_CAT_** EN EL DIRECTORIO LOCAL... DADO QUE DE ALGUNA FORMA SE QUEDA ESPERANDO ARGUMENTOS, PERO SI LO HACEMOS DESDE LA RAÍZ POR EJEMPLO:

Commands you may need to solve this level
[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)
## Referencias
- https://man7.org/linux/man-pages/man1/ls.1.html
- https://man7.org/linux/man-pages/man1/cd.1p.html
- https://man7.org/linux/man-pages/man1/cat.1.html
- https://man7.org/linux/man-pages/man1/file.1.html
- https://man7.org/linux/man-pages/man1/du.1.html
- https://man7.org/linux/man-pages/man1/find.1.html