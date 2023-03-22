# Bandit Level 25 → Level 26

## Objetivo

Iniciar sesión en bandit26 desde bandit25 debería ser bastante fácil... El shell para el usuario bandit26 no es **/bin/bash** , sino otra cosa. Descubra qué es, cómo funciona y cómo salir de él.

## Datos de acceso al nivel
- bandit25
- p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8dr
## Solucion
```
bandit25@bandit:~$ ls
bandit26.sshkey
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p
2220
_ _ _ _ ___ __
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
| |_) | (_| | | | | (_| | | |_ / /| (_) |
|_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
Connection to localhost closed.
bandit25@bandit:~$ cat /etc/passwd | grep bandit26
bandit26:x:11026:11026:bandit level
26:/home/bandit26:/usr/bin/showtext
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh
export TERM=linux
exec more ~/text.txt
exit 0
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p
2220
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
| |_) | (_| | | | | (_| | | |_ / /| (_) |
--More--(83%)
v
_ _ _ _ ___ __
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
| |_) | (_| | | | | (_| | | |_ / /| (_) |
"~/text.txt" [readonly] 6L, 258B
:e /etc/bandit_pass/bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
~
~
~
~
"/etc/bandit_pass/bandit26" [readonly] 1L, 33B
:!q
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
| |_) | (_| | | | | (_| | | |_ / /| (_) |
Press ENTER or type command to continue
q
~
~
------------------------
Connection to localhost closed.
bandit25@bandit:~ exit
```

## Notas adicionales
## Referencias
- https://mayadevbe.me/posts/overthewire/bandit/level25/