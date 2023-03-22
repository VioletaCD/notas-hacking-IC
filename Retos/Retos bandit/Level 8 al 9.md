# Bandit Level 8 → Level 9

## Objetivo

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once.

## Datos de acceso al nivel
- bandit8
- TESKZC0XvTetK0S9xNwm25STk5iWrBvP
## Solucion
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc data.txt
 1001  1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```

## Notas adicionales
  podemos redireccionar la salida del comando `sort` al comando `uniq -u` a través del símbolo `|`
## Referencias
- https://mundo-hackers.weebly.com/bandit.html
- https://www.w0lff4ng.org/wargame-bandit-1/