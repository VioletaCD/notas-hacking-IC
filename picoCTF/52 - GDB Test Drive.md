# GDB Test Drive
## Descripcipción
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/87/gdbme).Here's the test drive instructions:
-   `$ chmod +x gdbme`
-   `$ gdb gdbme`
-   `(gdb) layout asm`
-   `(gdb) break *(main+99)`
-   `(gdb) run`
-   `(gdb) jump *(main+104)`
## Pistas
- (None)
## Solucion
```
┌──(kali㉿kali)-[~/Documents/reversing/gdb]
└─$ gdb gdbme
(gdb) layout asm
-----------------------------------------------------------------------
			se abre una nueva ventana
-----------------------------------------------------------------------
(gdb) break *(main+99)
Breakpoint 1 at 0x132a
(gdb) run
Breakpoint 1, 0x00055555555532a in main ()
(gdb) jump *(main+104)
Continuing at 0x5555555552f.
picoCTF{d3bugg3r_dr1v3_7776d758}
[Inferior 1 (process 15650) exited normally]
(gdb)
```
## Bandera
picoCTF{d3bugg3r_dr1v3_7776d758}
## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=2Ncesy3mgLg