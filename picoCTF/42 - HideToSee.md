# HideToSee
## Descripcipción
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/237/atbash.jpg).
## Pistas
- Download the image and try to extract it.
## Solucion
```
──(kali㉿kali)-[~/Documents/crypto/hide]
└─$ file atbash.jpg 
atbash.jpg: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 465x455, components 3
┌──(kali㉿kali)-[~/Documents/crypto/hide]
└─$ steghide extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".    
┌──(kali㉿kali)-[~/Documents/crypto/hide]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_05y2z65z}

Nos ayudamos con cyberchef para terminar de desencryptar usando
-Atbash Cipher
```
## Bandera
picoCTF{atbash_crack_05b2a65a}
## Notas adicionales
instalar steghide en kali
## Referencias
- https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfMDV5Mno2NXp9Cg
- https://www.youtube.com/watch?v=yNFrsb5T5_s
