#  Insp3ct0r
## Descripcipción
Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/41511/` ([link](https://jupiter.challenges.picoctf.org/problem/41511/)) or http://jupiter.challenges.picoctf.org:41511
## Pistas
- How do you inspect web code on a browser?
- There's 3 parts
## Solucion
```
se ingresó a la pagina dada por el reto:
`https://jupiter.challenges.picoctf.org/problem/41511/` ([link](https://jupiter.challenges.picoctf.org/problem/41511/)) or http://jupiter.challenges.picoctf.org:41511

se revisa el codigo fuente de la pagina web:
en la cual se da la primera parte:
<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->

seguido se revisa [mycss.css](https://jupiter.challenges.picoctf.org/problem/41511/mycss.css)
encontrando dentro la segunda parte de la bandera:
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?832b0699} */

y la ultima parte se consiguió revisando
"[myjs.js](https://jupiter.challenges.picoctf.org/problem/41511/myjs.js)"

- encontrando la ultima parte de la bandera:
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */

>>> 
```
## Bandera
picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?832b0699}
## Notas adicionales
## Referencias
