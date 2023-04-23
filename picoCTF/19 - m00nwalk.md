# m00nwalk
## Descripcipción
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon
## Pistas
- How did pictures from the moon landing get sent back to Earth?
- What is the CMU mascot?, that might help select a RX option
## Solucion
```
-se descarga el archivo otorgado por el reto usando wget
wget https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav
-seguido de eso se instala la herramienta sstv para desencriptar el archivode audio
──(kali㉿kali)-[~/Documents/forense/M00N]
└─$ sudo git clone https://github.com/colaclanth/sstv.git
┌──(kali㉿kali)-[~/Documents/forense/M00N]
└─$ sudo python3 setup.py install  
-una vez instalado se pasa el archivo por el sstv
┌──(kali㉿kali)-[~/Documents/forense/M00N]
└─$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [##########################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!  
┌──(kali㉿kali)-[~/Documents/forense/M00N]
└─$ ls
message.wav  result.png
┌──(kali㉿kali)-[~/Documents/forense/M00N]
└─$ open result.png 
-consiguiendo la bandera dentro de una imagen
```

![[Pasted image 20230404164112.png]]
## Bandera
picoCTF{beep_boop_im_in_space}
## Notas adicionales
instalar sstv
## Referencias
https://github.com/colaclanth/sstv