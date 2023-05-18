# SQLLite
## Descripcipción
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).
## Pistas
- Don't tell anyone I told you this, but you can solve this problem without understanding the compare/jump relationship.
- Of course, if you're really good, you'll only need one attempt to solve this problem.
## Solucion
```
┌──(kali㉿kali)-[~/Documents/binary]
└─$  ls -la
total 28
drwxrwx--- 1 root vboxsf     0 may 16 22:33 .
drwxrwx--- 1 root vboxsf  4096 may 16 22:19 ..
-rwxrwx--- 1 root vboxsf 17088 may  9 16:19 local-target
-rwxrwx--- 1 root vboxsf   754 may  9 16:19 local-target.c
                                                                                  
┌──(kali㉿kali)-[~/Documents/binary]
└─$ file local-target  
local-target: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=63ee240a209d887ec451e996d844362e7e5c2078, for GNU/Linux 3.2.0, not stripped
                                                                                  
┌──(kali㉿kali)-[~/hacking/examen3]
└─$ file local-target.c 
local-target.c: C source, ASCII text

                                                                                  
┌──(kali㉿kali)-[~/hacking/examen3]
└─$ cat local-target.c
```
## Bandera
## Notas adicionales
## Referencias
