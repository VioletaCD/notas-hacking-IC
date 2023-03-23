# PW Crack 2

## Descripcipción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Pistas
- Does that encoding look familiar?
- The `str_xor` function does not need to be reverse engineered for this challenge.
## Solucion
```
┌──(kali㉿kali)-[~/Documents/2022]
└─$ cat level2.py   
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()

def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
    
level_2_pw_check()

┌──(kali㉿kali)-[~/Documents/2022]
└─$ python
Python 3.11.2 (main, Feb 12 2023, 00:48:52) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)
'4ec9'
>>> 

┌──(kali㉿kali)-[~/Documents/2022]
└─$ python level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```
## Bandera
picoCTF{tr45h_51ng1ng_9701e681}
## Notas adicionales
en este caso se corre el programa de python y nos pide una contraseña, se le realiza un cat a este y nos muestra el codigo el el cual esta el password encriptado el cual se da a conocer usando python
## Referencias
https://www.youtube.com/watch?v=hdtQHEFBQh0