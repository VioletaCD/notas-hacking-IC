# Plumbing
## Descripcipción
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 7480`.
## Pistas
- Remember the flag format is picoCTF{XXXX}
- What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)
## Solucion
```
┌──(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 7480 >> flagout.txt
                                                                            
┌──(kali㉿kali)-[~]
└─$ ls    
Desktop    Downloads  flagout.txt  Music     Public     token
Documents  file       haking       Pictures  Templates  Videos
                                                                            
┌──(kali㉿kali)-[~]
└─$ cat flagout.txt | grep pico
picoCTF{digital_plumb3r_06e9d954}

```
## Bandera
picoCTF{digital_plumb3r_06e9d954}
## Notas adicionales
Lo que hace una tubería en Shell es que nos permite combinar dos comandos en uno. Entonces, si quisiéramos grep el valor de retorno de la conexión del host netcat para un indicador, podemos ejecutar `nc 2019shell1.picoctf.com 9525 | grep picoCTF`.

## Referencias
- http://www.linfo.org/pipes.html