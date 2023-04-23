# Codebook
## Descripcipción
Run the Python script `code.py` in the same directory as `codebook.txt`.
-   [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)
## Pistas
- On the webshell, use `ls` to see if both files are in the directory you are in
- The `str_xor` function does not need to be reverse engineered for this challenge.
## Solucion
```
┌──(kali㉿kali)-[~/Documents]
└─$ cd 2022     
                                                                            
┌──(kali㉿kali)-[~/Documents/2022]
└─$ ls
codebook.txt  code.py
                                                                            
┌──(kali㉿kali)-[~/Documents/2022]
└─$ python3 code.py
picoCTF{c0d3b00k_455157_7d102d7a}
```
## Bandera
picoCTF{c0d3b00k_455157_7d102d7a}

## Notas adicionales
Se descarga el script de python dado y se ejecuta usando python3. 
## Referencias
https://infosecwriteups.com/beginner-picomini-ctf-2022-writeup-94174d0ea64b
