# vault-door-4
## Descripcipción
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/09d3002ae349631324a17e2255ae8df2/VaultDoor4.java)
## Pistas
- Use a search engine to find an "ASCII table".
- You will also need to know the difference between octal, decimal, and hexadecimal numbers.
## Solucion
```
Usando JAVA SCRIPT
String.fromCharCode(106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 0143, 061 ) + ['9' , '4' , 'f' , '7' , '4' , '5' , '8' , 'e'].join('')
        "jU5t_4_bUnCh_0f_bYt3s_c194f7458e"

```
## Bandera
picoCTF{jU5t_4_bUnCh_0f_bYt3s_c194f7458e}
## Notas adicionales
## Referencias
