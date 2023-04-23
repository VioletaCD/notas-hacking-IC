# Fixme1.py
## Descripcipción
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Pistas
- Indentation is very meaningful in Python
- To view the file in the webshell, do: `$ nano fixme1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.
## Solucion
```
┌──(kali㉿kali)-[~/Documents/2022]
└─$ python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}

```
## Bandera
picoCTF{1nd3nt1ty_cr1515_6a476c8f}
## Notas adicionales
Para solucionar el reto abrí el codigo en algun editor de texto, seguido de ahi borre la sangría de Print la cual no está permitida en python. 
## Referencias
https://www.youtube.com/watch?v=UTLFMjrMfa8