# MacroHard WeakEdge
## Descripcipción
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/c0da20f29337e87ffb58ea987d8c596e/Forensics%20is%20fun.pptm)
## Pistas
None
## Solucion
```
-DESCARGAR LOS DOS ARCHIVOS DEL RETO
┌──(kali㉿kali)-[~/Documents/forense/macro]
└─$ wget https://mercury.picoctf.net/static/c0da20f29337e87ffb58ea987d8c596e/Forensics%20is%20fun.pptm

-instalamos el VISUAL CODE
- EN ESTE ABRIMOS EL ARCHIVO Y ENCONTRAMOS UNA CADENA EN BASE 64 LA CUAL LLEVAMOS A LA TERMIAL PARA OBTENER LA BANDERA

┌──(kali㉿kali)-[~/Documents/forense/macro]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " "
ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ

┌──(kali㉿kali)-[~/Documents/forense/macro]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " " | base64 -d    
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
┌──(kali㉿kali)-[~/Documents/forense/macro]
└─$ 
```
## Bandera
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
## Notas adicionales
## Referencias
- https://support.microsoft.com/en-us/office/file-formats-that-are-supported-in-powerpoint-252c6fa0-a4bc-41be-ac82-b77c9773f9dc#:~:text=The%20default%20file%20format%20in,pptx.&text=A%20presentation%20that%20you%20can,device%20that%20has%20PowerPoint%20installed
- https://www.youtube.com/watch?v=CsCeOp9PFGs&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=28
