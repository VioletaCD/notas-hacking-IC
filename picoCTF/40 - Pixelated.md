# Pixelated
## Descripcipción
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/1594c3f1980e3fb93df09a6d02f53904/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/1594c3f1980e3fb93df09a6d02f53904/scrambled2.png)
## Pistas
- [https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
- Think of different ways you can "stack" images
## Solucion
```
-PRIMERA SOLUCIÓN USANDO LA HERRAMIENTA
stegsolve.jar
-se cargan ambas imagenes y se le da en unir y muestra todas sus posibles opciones hasta mostrar la bandera

--SEGUNDA SOLUCIÓN
Usando python
from PIL import Image
import numpy as np
imagen1 = np.asarray(Image.open('scrambled1.png'))
imagen2 = np.asarray(Image.open('scrambled2.png'))

print(imagen1)
print(imagen2)

datos = imagen1.copy() + imagen1.copy()
nueva = Image.fromarray(datos
nueva.save('nueva.png','PNG')
```
![[Pasted image 20230427203617.png]]
## Bandera
picoCTF{1b867c3e}
## Notas adicionales
## Referencias
[https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
https://www.youtube.com/watch?v=zWU6MV8dQQ4
