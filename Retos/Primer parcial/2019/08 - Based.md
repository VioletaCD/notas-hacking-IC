# Based
## Descripcipción
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.
## Pistas
- I hear python can convert things.
- It might help to have multiple windows open.
## Solucion
```
┌──(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 29221.
Let us see how data is stored
light
Please give the 01101100 01101001 01100111 01101000 01110100 as a word.
...
you have 45 seconds.....

Input:
light
Please give me the  163 165 142 155 141 162 151 156 145 as a word.
Input:
submarine
Please give me the 6c69676874 as a word.
Input:
light
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}
```
## Bandera
picoCTF{learning_about_converting_values_00a975ff}
## Notas adicionales
 Después de algunos intentos, podemos notar que los números tienen diferentes bases y es necesario convertirlos a ASCII para obtener estas palabras. Las preguntas también están cronometradas y aleatorias, por lo que debe seguir su tiempo.

## Referencias
https://www.youtube.com/watch?v=PPZPnQRn9rM

