# Wave a flag
## Descripcipción
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) has extraordinarily helpful information...
## Pistas
- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm`
- Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.
## Solucion
```
┌──(kali㉿kali)-[~]
└─$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
--2023-03-22 18:23:38--  https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: ‘warm.1’

warm.1             100%[================>]  10.68K  --.-KB/s    in 0s      

2023-03-22 18:23:38 (84.2 MB/s) - ‘warm.1’ saved [10936/10936]

                                                                            
┌──(kali㉿kali)-[~]
└─$ ls
Desktop    Downloads  flagout.txt  Music     Public     token   warm
Documents  file       haking       Pictures  Templates  Videos  warm.1
                                                                            
┌──(kali㉿kali)-[~]
└─$ ./ warm
zsh: permission denied: ./
                                                                            
┌──(kali㉿kali)-[~]
└─$ ./warm 
zsh: permission denied: ./warm
                                                                            
┌──(kali㉿kali)-[~]
└─$ chmod +x warm                                   
                                                                            
┌──(kali㉿kali)-[~]
└─$ ./warm
Hello user! Pass me a -h to learn what I can do!
                                                                            
┌──(kali㉿kali)-[~]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}

```
## Bandera
picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
## Notas adicionales
Uno puede usar el comando de strings para obtener todas las cadenas en el archivo y luego guardar todas las cadenas en un archivo txt y luego usar la opción gedit find para encontrar la bandera.  
encuentre la cadena de filtro que se usará: picoCTF{ (como sabemos, todas las banderas comenzarían solo con esta cadena)

A veces es bueno pensar fuera del tema, puede hacer que la vida sea más fácil, pero no siempre tendrá éxito.

## Referencias
https://medium.com/@arthDetroja/picoctf-write-up-wave-a-flag-fc1f42dc5d4d
