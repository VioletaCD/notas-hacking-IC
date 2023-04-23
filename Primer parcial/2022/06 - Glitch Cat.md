# Glitch Cat
## Descripcipción
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 50363`
## Pistas
- ASCII is one of the most common encodings used in programming
- We know that the glitch output is valid Python, somehow!
- Press Ctrl and c on your keyboard to close your connection and return to the command prompt.
## Solucion
```
┌──(kali㉿kali)-[~/Documents/2022]
└─$ nc saturn.picoctf.net 50363
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
┌──(kali㉿kali)-[~/Documents/2022]
└─$ python           
Python 3.11.2 (main, Feb 12 2023, 00:48:52) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> x = picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}
  File "<stdin>", line 1
    x = picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}
               ^
SyntaxError: invalid syntax
>>> x = 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
>>> x = 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
>>> x
'picoCTF{gl17ch_m3_n07_a4392d2e}'
>>> 
```
## Bandera
picoCTF{gl17ch_m3_n07_a4392d2e}
## Notas adicionales
En este caso se ejecuta en la linea de comandos la linea dada por el reto, y muestra 
parte de la bandera, se abre la terminal de python y se iguala con X lo  que se obtuvo de ejecutar la linea del reto, se corre de nuevo y muestra la bandera.
## Referencias
https://www.youtube.com/watch?v=PJSTTNG7Ig0