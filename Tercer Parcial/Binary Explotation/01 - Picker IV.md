# Picker IV
## Descripcipción
Can you figure out how this program works to get the flag?Connect to the program with netcat:`nc saturn.picoctf.net 60711`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV).
## Pistas
- With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.
- How can you find the address that `win` is at?
## Solucion
```
┌──(kali㉿kali)-[~/Documents/binary/picker]
└─$ ls -la
total 32
drwxr-xr-x 2 kali kali  4096 May 15 17:26 .
drwxr-xr-x 8 kali kali  4096 May 15 17:25 ..
-rw-r--r-- 1 kali kali 17272 May  9 18:20 picker-IV
-rw-r--r-- 1 kali kali   839 May  9 18:20 picker-IV.c
                                                                     
┌──(kali㉿kali)-[~/Documents/binary/picker]
└─$ file picker-IV
picker-IV: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=12b33c5ff389187551aae5774324da558cee006c, for GNU/Linux 3.2.0, not stripped
                                                                     
┌──(kali㉿kali)-[~/Documents/binary/picker]
└─$ chmod +x picker-IV
                                                                     
┌──(kali㉿kali)-[~/Documents/binary/picker]
└─$ gdb picker-IV
GNU gdb (Debian 13.1-2) 13.1
Copyright (C) 2023 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from picker-IV...
(No debugging symbols found in picker-IV)
(gdb) Quit
(gdb) quit
                                                                     
┌──(kali㉿kali)-[~/Documents/binary/picker]
┌──(kali㉿kali)-[~/Documents/binary/picker]
└─$ ls    
picker-IV  picker-IV.c
                                                                     
┌──(kali㉿kali)-[~/Documents/binary/picker]
└─$ ./picker-IV 
Enter the address in hex to jump to, excluding '0x': hola
You input 0x0
Segfault triggered! Exiting.
                                                                     
┌──(kali㉿kali)-[~/Documents/binary/picker]
└─$ gdb picker-IV
GNU gdb (Debian 13.1-2) 13.1
Copyright (C) 2023 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from picker-IV...
(No debugging symbols found in picker-IV)
(gdb) break win
Breakpoint 1 at 0x4012a6
(gdb) run
Starting program: /home/kali/Documents/binary/picker/picker-IV 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".                                                                
Enter the address in hex to jump to, excluding '0x': 0xdeadbeef
You input 0xdeadbeef

Program received signal SIGSEGV, Segmentation fault.
0x00000000deadbeef in ?? ()
(gdb) info address win
Symbol "win" is at 0x40129e in a file compiled without debugging.
(gdb) set $rip=<0x40129e>
A syntax error in expression, near `<0x40129e>'.
(gdb) set $rip=<0x40129e>
A syntax error in expression, near `<0x40129e>'.
(gdb) set $rip=0x40129e
(gdb) continue
Continuing.
Segfault triggered! Exiting.

[Inferior 1 (process 65650) exited with code 013]
(gdb) 
The program is not being run.
(gdb) quit

┌──(kali㉿kali)-[~/Documents/binary/picker]
└─$ nc saturn.picoctf.net 60711
Enter the address in hex to jump to, excluding '0x': 0x40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}
```
## Bandera
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}
## Notas adicionales
## Referencias
