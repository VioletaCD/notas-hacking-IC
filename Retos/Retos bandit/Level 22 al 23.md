## Level 22 → Level 23

## Objetivo
Un programa se ejecuta automáticamente a intervalos regulares desde **cron** , el programador de trabajos basado en el tiempo. Busque en **/etc/cron.d/** la configuración y vea qué comando se está ejecutando.

**NOTA:** Mirar scripts de shell escritos por otras personas es una habilidad muy útil. El guión para este nivel se hace fácil de leer intencionalmente. Si tiene problemas para comprender lo que hace, intente ejecutarlo para ver la información de depuración que imprime.
## Datos de acceso al nivel
- bandit22 
- WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
## Solucion
```
bandit22@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ whoami
bandit22
bandit22@bandit:~$ myname=bandit23
bandit22@bandit:~$ echo $(echo I am user $myname | md5sum | cut -d ' ' -f 1)
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```

## Notas adicionales
Visitamos cron nuevamente, esta vez el script que ejecuta cron es un poco más complicado. Crea un archivo en /tmp que es el resultado de un proceso de hashing md5 combinado con un nombre de usuario que crea el nombre del archivo que contendrá la contraseña. En otras palabras, cuando se ejecute, proporcionará el nombre del archivo en el directorio /tmp en el que se va a volcar la contraseña.
## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/
