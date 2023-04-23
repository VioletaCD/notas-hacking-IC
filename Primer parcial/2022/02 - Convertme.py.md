# Convertme.py
## Descripcipción
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)https://artifacts.picoctf.net/c/34/runme.py)
## Pistas
- Look up a decimal to binary number conversion app on the web or use your computer's calculator!
- The `str_xor` function does not need to be reverse engineered for this challenge.
- If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
- To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
- Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
- Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 convertme.py`
## Solucion
```
┌──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/23/convertme.py
--2023-03-22 22:04:51--  https://artifacts.picoctf.net/c/23/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.40, 99.84.203.115, 99.84.203.9, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: ‘convertme.py.1’

convertme.py.1                            100%[====================================================================================>]   1.16K  --.-KB/s    in 0s      

2023-03-22 22:04:52 (14.0 MB/s) - ‘convertme.py.1’ saved [1189/1189]

                                                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ ls                                                  
convertme.py    Desktop    Downloads  flagout.txt  ltdis.sh  Pictures  static                    static.ltdis.x86_64.txt  token   warm
convertme.py.1  Documents  file       haking       Music     Public    static.ltdis.strings.txt  Templates                Videos  warm.1
                                                                                                                                                                       
┌──(kali㉿kali)-[~]
└─$ python convertme.py                                 
If 70 is in decimal base, what is it in binary base?
---------------------------------------------------------------------------
┌──(kali㉿kali)-[~]
└─$ python
Python 3.11.2 (main, Feb 12 2023, 00:48:52) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bin(70)
'0b1000110'
--------------------------------------------------------------------------
Answer: 1000110
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}



```
## Bandera
picoCTF{4ll_y0ur_b4535_9c3b7d4d}
## Notas adicionales
se resuelve con una conversion de binario a texto

## Referencias
