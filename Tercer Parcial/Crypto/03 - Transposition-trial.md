# Transposition-trial
## Descripcipción
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/193/message.txt)
## Pistas
- Split the message up into blocks of 3 and see how the first block is scrambled
## Solucion
```
┌──(kali㉿kali)-[~/Documents/crypto/transposition-trial]
└─$ ls    
message.txt
┌──(kali㉿kali)-[~/Documents/crypto/transposition-trial]
└─$ cat message.txt 
┌──(kali㉿kali)-[~/Documents/crypto/transposition-trial]
└─$ touch trans.py   
┌──(kali㉿kali)-[~/Documents/crypto/transposition-trial]
└─$ sudo nano trans.py
┌──(kali㉿kali)-[~/Documents/crypto/transposition-trial]
└─$ python3 trans.py              
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}

-------------------------------------------------------------------------
								trans.py
-------------------------------------------------------------------------
MESSAGE = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V9AAB1F8}7"

FLAG=""
for i in range(0, len (MESSAGE), 3):
        FLAG += MESSAGE[i + 2] + MESSAGE[i:i + 2]

print(FLAG)
```
## Bandera
picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}
## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=ZTQAc28BfFw