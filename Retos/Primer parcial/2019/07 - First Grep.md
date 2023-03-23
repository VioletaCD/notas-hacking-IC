# First Grep
## Descripcipción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Pistas
grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)
## Solucion
```
┌──(kali㉿kali)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
--2023-03-22 15:11:02--  https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: ‘file’

file               100%[===============>]  14.21K  --.-KB/s    in 0s      

2023-03-22 15:11:03 (41.9 MB/s) - ‘file’ saved [14551/14551]

                                                                           
┌──(kali㉿kali)-[~]
└─$ cat file | grep pico                            
picoCTF{grep_is_good_to_find_things_dba08a45}

```
## Bandera
picoCTF{grep_is_good_to_find_things_dba08a45}
## Notas adicionales
Cuando simplemente `cat`este archivo en el shell para encontrar la bandera, nos encontramos con una gran cantidad de ruido aleatorio. Aquí, podemos usar un `grep`comando. Lo que `grep`hace es filtrar una expresión específica en un texto sin formato. Sabemos que las banderas de picoCTF están todas en el formato de picoCTF{...}, por lo que podemos buscar la expresión grep `picoCTF`. Específicamente, haríamos `cat file | grep picoCTF`.

## Referencias
https://ryanstutorials.net/linuxtutorial/grep.php
