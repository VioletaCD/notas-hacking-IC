# Tab, Tab, Attack
## Descripcipción
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip)
## Pistas
- After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...
## Solucion
```
                                                                            
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls fang-of-haynekhtnamet 
fang-of-haynekhtnamet
                                                                            
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ chmod +x ltdis.sh
                                                                            
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ chmod +x fang-of-haynekhtnamet
                                                                            
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls fang-of-haynekhtnamet
fang-of-haynekhtnamet
                                                                            
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}

```
## Bandera
picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}
## Notas adicionales
Descomprima todo y luego diviértase navegando usando `ls`para enumerar las carpetas/archivos y `cd <foldername>`navegar hasta allí. Eventualmente habrá un [archivo ELF](https://github.com/vivian-dai/PicoCTF2021-Writeup/blob/main/General%20Skills/Tab%2C%20Tab%2C%20Attack/fang-of-haynekhtnamet) con el nombre `fang-of-haynekhtnamet` `./fang-of-haynekhtnamet`para ejecutarlo. Produce: `*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}`

## Referencias
https://www.youtube.com/watch?v=8SCV87IC11c
