# WebNet0
## Descripcipción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
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

- LO ABRIMOS CON WIRESHAR y realizamos una busqueda y asi obtenemos la bandera
```
## Bandera
picoCTF{nongshim.shrimp.crackers}
## Notas adicionales
## Referencias
https://en.wikipedia.org/wiki/Transport_Layer_Security
https://www.youtube.com/watch?v=9uflLPoETOc&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=24