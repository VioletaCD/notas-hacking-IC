# Extensions
## Descripcipción
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Pistas
- How do operating systems know what kind of file it is? (It's not just the ending!
- Make sure to submit the flag as picoCTF{XXXXX}
## Solucion
```
┌──(kali㉿kali)-[~/Documents/forense]
└─$ cd extension
┌──(kali㉿kali)-[~/Documents/forense/extension]
└─$ wget https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt    
--2023-03-23 20:44:38--  https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9984 (9.8K) [application/octet-stream]
Saving to: ‘flag.txt’

flag.txt                                  100%[=================================================

2023-03-23 20:44:39 (156 MB/s) - ‘flag.txt’ saved [9984/9984]

┌──(kali㉿kali)-[~/Documents/forense/extension]
└─$ file flag.txt    
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
┌──(kali㉿kali)-[~/Documents/forense/extension]
└─$ xxd flag.txt | head
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR
00000010: 0000 06a1 0000 0260 0802 0000 0085 ad5e  .......`.......^
00000020: 9a00 0000 0173 5247 4200 aece 1ce9 0000  .....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 0000 1625 0000 1625 0149  ..pHYs...%...%.I
00000050: 5224 f000 0026 9549 4441 5478 5eed dd6b  R$...&.IDATx^..k
00000060: 421b 39b7 05d0 3b2e 0694 f130 9a4c 2683  B.9...;....0.L&.
00000070: f9ae 5f80 4e3d 25bb 4cb3 f15a bfba a14a  .._.N=%.L..Z...J
00000080: 7574 2413 7927 c0ff fd0f 0000 0000 4826  ut$.y'........H&
00000090: e303 0000 0080 6c32 3e00 0000 00c8 26e3  ......l2>.....&.
┌──(kali㉿kali)-[~/Documents/forense/extension]
└─$ mv flag.txt flag.png 
┌──(kali㉿kali)-[~/Documents/forense/extension]
└─$ open flag.png 
┌──(kali㉿kali)-[~/Documents/forense/extension]

```
## Bandera
picoCTF{now_you_know_about_extensions}
## Notas adicionales
La llave es encontrada dentro del archivo png despues de revisar el txt y verificar que dentro tenia un png, esto solo implicó cambiar la extensión
## Referencias
