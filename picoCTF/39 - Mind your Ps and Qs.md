#  Mind your Ps and Qs
## Descripcipción
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/51d68e61bb41207a55f24e753f07c5a3/values)
## Pistas
- Bits are expensive, I used only a little bit over 100 to save money
## Solucion
```
┌──(kali㉿kali)-[~]
└─$ python3
Python 3.11.2 (main, Mar 13 2023, 12:18:29) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> 
>>> c=62324783949134119159408816513334912534343517300880137691662780895409992760262021
>>> e=65537
>>> p=1899107986527483535344517113948531328331
>>> q=674357869540600933870145899564746495319033
>>> n=p*q
>>> n
1280678415822214057864524798453297819181910621573945477544758171055968245116423923
>>> tn = (p-1)*(q-1)
>>> d=inverse(e,tn)
>>> m=pow(c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639555654677400177227645
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_05012767}'

```
## Bandera
picoCTF{sma11_N_n0_g0od_05012767}
## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=pwGSp_4YHTg