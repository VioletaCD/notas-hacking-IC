# Bandit Level 14 → Level 15

## Objetivo

La contraseña para el siguiente nivel se puede recuperar enviando la contraseña del nivel actual al **puerto 30000 en localhost** .

## Datos de acceso al nivel
- bandit14 
- fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
## Solucion
```
bandit14@bandit:~$ telnet localhost 30000
Trying 127.0.0.1...
Connected to localhost.
Escape character is '^]'.
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

Connection closed by foreign host.
bandit14@bandit:~$

```

## Notas adicionales
Aquí tenemos una lección de telnet. Básicamente, usamos telnet para conectarnos a localhost en el puerto 30000 e ingresar la contraseña mientras todavía estamos en el shell de bandit14.
## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/
- https://www.ibm.com/docs/es/aix/7.1?topic=protocols-telnet-protocol
