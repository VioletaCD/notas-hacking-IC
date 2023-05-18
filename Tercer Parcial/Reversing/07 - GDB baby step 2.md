# GDB baby step 2
## Descripcipción
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Debug [this](https://artifacts.picoctf.net/c/520/debugger0_b).
## Pistas
- You could calculate `eax` yourself, or you could set a breakpoint for after the calculcation and inspect `eax` to let the program do the heavy-lifting for you
## Solucion
```
──(kali㉿kali)-[~/Documents/reversing/baby1]
┌──(kali㉿kali)-[~/Documents/reversing/baby1]
└─$ ls
debugger0_a
                                                                           
┌──(kali㉿kali)-[~/Documents/reversing/baby1]
└─$ file debugger0_a 
debugger0_a: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=15a10290db2cd2ec0c123cf80b88ed7d7f5cf9ff, for GNU/Linux 3.2.0, not stripped
                                                                           
┌──(kali㉿kali)-[~/Documents/reversing/baby1]
└─$ ls
debugger0_a
                                                                           
┌──(kali㉿kali)-[~/Documents/reversing/baby1]
└─$ cat debugger0_a 
```
## Bandera
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}
## Notas adicionales
## Referencias
