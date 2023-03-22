## Level 21 → Level 22

## Objetivo
Un programa se ejecuta automáticamente a intervalos regulares desde **cron** , el programador de trabajos basado en el tiempo. Busque en **/etc/cron.d/** la configuración y vea qué comando se está ejecutando.

**NOTA:** intente conectarse a su propio demonio de red para ver si funciona como cree

## Datos de acceso al nivel
- bandit21 
- NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
## Solucion
```
bandit21@bandit:~$ ls -la /etc/cron.d
total 56
drwxr-xr-x   2 root root  4096 Feb 21 22:04 .
drwxr-xr-x 108 root root 12288 Feb 21 22:04 ..
-rw-r--r--   1 root root    62 Feb 21 22:02 cronjob_bandit15_root
-rw-r--r--   1 root root    62 Feb 21 22:02 cronjob_bandit17_root
-rw-r--r--   1 root root   120 Feb 21 22:03 cronjob_bandit22
-rw-r--r--   1 root root   122 Feb 21 22:03 cronjob_bandit23
-rw-r--r--   1 root root   120 Feb 21 22:03 cronjob_bandit24
-rw-r--r--   1 root root    62 Feb 21 22:03 cronjob_bandit25_root
-rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
-rwx------   1 root root    52 Feb 21 22:04 otw-tmp-dir
-rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
-rw-r--r--   1 root root   396 Feb  2  2021 sysstat
bandit21@bandit:~$ cat  /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ man 5 crontab
bandit21@bandit:~$ cat  /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
```

## Notas adicionales
 Tras la inspección del directorio cron, vemos un trabajo en la lista para bandit22. El contenido muestra que ejecuta un script que descarga la contraseña de bandit22 en un archivo en /tmp. Mirar el contenido de ese archivo revela la contraseña de bandit22.
## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/
