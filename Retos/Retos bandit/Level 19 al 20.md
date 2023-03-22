# Bandit Level 19 → Level 20

## Objetivo

Para obtener acceso al siguiente nivel, debe usar el binario setuid en el directorio de inicio. Ejecutarlo sin argumentos para saber cómo usarlo. La contraseña para este nivel se puede encontrar en el lugar habitual (/etc/bandit_pass), después de haber utilizado el binario setuid.

## Datos de acceso al nivel
- bandit19 
- awhqfNnAbc1naukrpqDYcF95h7HoMTrC
## Solucion
```
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rwsr-x---  1 bandit20 bandit19 14876 Feb 21 22:03 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
bandit19@bandit:~$  ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$
```

## Notas adicionales
El binario suid se ejecuta como bandit20, por lo que podemos aprovechar esto para ver la contraseña de bandit20 como bandit19.
## Referencias
- https://en.wikipedia.org/wiki/Setuid
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/
