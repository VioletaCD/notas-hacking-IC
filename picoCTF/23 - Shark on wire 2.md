# Shark on wire 2
## Descripcipción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
## Pistas
None
## Solucion
```
-DESCARGAR EL ARCHIVO DEL RETO
┌──(kali㉿kali)-[~/Documents/forense/shark]
└─$ wget https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap

-REVISAMOS SU CONTENIDO
┌──(kali㉿kali)-[~/Documents/forense/shark]
└─$ file capture.pcap                                       
capture.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
- LO ABRIMOS CON WIRESHARK
┌──(kali㉿kali)-[~/Documents/forense/shark]
└─$ wireshark capture.pcap &
[1] 40151

--para obtimizar el proceso de busqueda de la bandera se hace lo siguiente 

┌──(kali㉿kali)-[~/Documents/forense/shark]
└─$ nano exp.py  
┌──(kali㉿kali)-[~]
└─$ cd Documents/forense/shark
┌──(kali㉿kali)-[~/Documents/forense/shark]
└─$ python3 -m pip install scapy
Defaulting to user installation because normal site-packages is not writeable
Requirement already satisfied: scapy in /usr/lib/python3/dist-packages (2.5.0)

--------------------------exp.py------------------------------------------
flag = ''

for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)
----------------------------------------------------------------------------

──(kali㉿kali)-[~/Documents/forense/shark]
└─$ python3 exp.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```
## Bandera
picoCTF{p1LLf3r3d_data_v1a_st3g0}
## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=WcMl1SvQ6hI&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=23
