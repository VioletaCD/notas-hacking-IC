# Rotation
## Descripcipción
You will find the flag after decrypting this fileDownload the encrypted flag [here](https://artifacts.picoctf.net/c/391/encrypted.txt).
## Pistas
- Sometimes rotation is right
## Solución
```
┌──(kali㉿kali)-[~/Documents]
└─$ cat encrypted.txt | tr [a-zA-Z] [s-za-rS-ZA-R]
picoCTF{r0tat1on_d3crypt3d_7d140864}
┌──(kali㉿kali)-[~/Documents]
└─$
```
## Bandera
picoCTF{r0tat1on_d3crypt3d_7d140864}
## Notas Adicionales
## Referencias
