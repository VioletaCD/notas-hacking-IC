#  Wireshark doo dooo do doo...
## Descripcipción
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/ea41c400c3c7b4a63406e5e607d362ab/shark1.pcapng).
## Pistas
(none)
## Solucion
```
- abrimos el archivo con wireshark
- seleccionamos la pestaña statics
- seleccionamos Protocol Hierarchy
- seleccionar Line-based text date
- seleccionar Apply as Filter
- presionar selected y close
- en el primer filtro presionar click izquierdo e ir a follow
- seleccionar TCP Stream
- tomar la llave Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}
- y aplicar ROT13
```
## Bandera
picoCTF{p33kab00_1_s33_u_deadbeef}

## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=23w3gtrJV9U