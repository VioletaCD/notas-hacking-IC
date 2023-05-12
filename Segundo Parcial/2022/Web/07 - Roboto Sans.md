# Roboto Sans 
## Descripcipción
The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:64271/) out
## Pistas
- (None)
## Solucion
```
Para obtener la bandera:
- ingresar a la pagina
- agregar al final del link robots.txt // ENCONTRANDO LO SIGUIENTE
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/

- al no coincidir nada con el formato de la bandera se toma el siguiete fracmento decodificandolo en base 64 
	"anMvbXlmaWxlLnR4dA=="
- otorga una nueva extension
	"js/myfile.txt"
- Se agrega al link quitando la parte de robots para encontrar la bandera
```
![[Pasted image 20230504181815.png]]
## Bandera
picoCTF{Who_D03sN7_L1k5_90B0T5_032f1c2b}
## Notas adicionales
## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,true)&input=YW5NdmJYbG1hV3hsTG5SNGRBPT0
https://www.youtube.com/watch?v=BBkhYcdKBLE

