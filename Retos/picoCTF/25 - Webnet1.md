# WebNet1
## Descripcipción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Pistas
- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?
## Solucion
```
-DESCARGAR LOS DOS ARCHIVOS DEL RETO
┌──(kali㉿kali)-[~/Documents/forense/webNt]
└─$ wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
┌──(kali㉿kali)-[~/Documents/forense/webNt]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key'
-REVISAMOS SU CONTENIDO
┌──(kali㉿kali)-[~/Documents/forense/webNt]
└─$ ls -la
total 28
drwxr-xr-x 2 kali kali  4096 Apr  4 20:17 .
drwxr-xr-x 7 kali kali  4096 Apr  4 20:15 ..
-rw-r--r-- 1 kali kali 13163 Oct 26  2020 capture.pcap
-rw-r--r-- 1 kali kali  1704 Oct 26  2020 picopico.key

- LO ABRIMOS CON WIRESHAR 
- Descargamos la imagen que se encuentra en el paquete 47 la abrimos y revisamos y encotramos la bandera

┌──(kali㉿kali)-[~/Documents/forense/webNt1]
└─$ open vulture.jpg 
                                                                            
┌──(kali㉿kali)-[~/Documents/forense/webNt1]
└─$ strings vulture.jpg -n15     
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz

```
## Bandera
picoCTF{honey.roasted.peanuts}
## Notas adicionales
## Referencias
https://en.wikipedia.org/wiki/Transport_Layer_Security
https://www.youtube.com/watch?v=Ym3i79nEHjw&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=25