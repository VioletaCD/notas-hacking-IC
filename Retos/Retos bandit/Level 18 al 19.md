# Bandit Level 11 → Level 12

## Objetivo

La contraseña para el siguiente nivel se almacena en un archivo **Léame** en el directorio de inicio. Desafortunadamente, alguien ha modificado **.bashrc** para cerrar la sesión cuando inicia sesión con SSH.

## Datos de acceso al nivel
- bandit18
- hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
## Solucion
```
- SOLUCIÓN 1
C:\Users\vayol>ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
awhqfNnAbc1naukrpqDYcF95h7HoMTrC


SOLUCIÓN 2
C:\Users\vayol>ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
cat readme
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```

## Notas adicionales
## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/