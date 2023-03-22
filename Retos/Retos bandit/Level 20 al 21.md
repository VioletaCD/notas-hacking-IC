## Level 20 → Level 21

## Objetivo

Hay un binario setuid en el directorio de inicio que hace lo siguiente: establece una conexión con localhost en el puerto que especifique como argumento de la línea de comandos. Luego lee una línea de texto de la conexión y la compara con la contraseña del nivel anterior (bandit20). Si la contraseña es correcta, transmitirá la contraseña para el siguiente nivel (bandit21).

**NOTA:** intente conectarse a su propio demonio de red para ver si funciona como cree

## Datos de acceso al nivel
- bandit20 
- VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solucion
```
bandit20@bandit:~$ nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 3123209
bandit20@bandit:~$ Listening on 0.0.0.0 2020

bandit20@bandit:~$  ./suconnect 2020
Connection received on 127.0.0.1 58350
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
```

## Notas adicionales
 Este es un poco más complicado. Al ingresar al shell de bandit20, vemos un binario que se conecta a un puerto local y espera que se le envíe una conexión y la contraseña desde el exterior. Necesitamos dos proyectiles para lograr esto.
## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/