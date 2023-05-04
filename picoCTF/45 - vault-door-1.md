# vault-door-1
## Descripcipción
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/29b91e638ccbd76aaa8c0462d1c64d8d/VaultDoor1.java)
## Pistas
- Look up the charAt() method online.
## Solucion
```
se toma parte del codigo dado y se modifica de forma manual de la siguiente forma:
	       password.charAt(00)  == 'd' &&
               password.charAt(29) == '3' &&
               password.charAt(04)  == 'r' &&
               password.charAt(02)  == '5' &&
               password.charAt(23) == 'r' &&
               password.charAt(03)  == 'c' &&
               password.charAt(17) == '4' &&
               password.charAt(01)  == '3' &&
               password.charAt(07)  == 'b' &&
               password.charAt(10) == '_' &&
               password.charAt(05)  == '4' &&
               password.charAt(09)  == '3' &&
               password.charAt(11) == 't' &&
               password.charAt(15) == 'c' &&
               password.charAt(08)  == 'l' &&
               password.charAt(12) == 'H' &&
               password.charAt(20) == 'c' &&
               password.charAt(14) == '_' &&
               password.charAt(06)  == 'm' &&
               password.charAt(24) == '5' &&
               password.charAt(18) == 'r' &&
               password.charAt(13) == '3' &&
               password.charAt(19) == '4' &&
               password.charAt(21) == 'T' &&
               password.charAt(16) == 'H' &&
               password.charAt(27) == 'f' &&
               password.charAt(30) == 'b' &&
               password.charAt(25) == '_' &&
               password.charAt(22) == '3' &&
               password.charAt(28) == '6' &&
               password.charAt(26) == 'f' &&
               password.charAt(31) == '0'
------------------------------------------------------------------------------
Una vez modificado se guarda el archivo y se digitan los siguientes comandos:
┌──(kali㉿kali)-[~/Documents/reversing/vaultdoor1]
└─$ cat labandera | sort | awk '{print($3)}' | tr -d "'" | tr -d "\n"
d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0 

-SE OBTIENE LA BANDERA Y PARA COMPROBAR QUE ES CORRECTA SE EJECUTA EL PROGRAMA
Y SE INGRESE LA BANDERA EN EL FORMATO picoCTF{}
┌──(kali㉿kali)-[~/Documents/reversing/vaultdoor1]
└─$ java VaultDoor1
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Enter vault password: picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0}
Access granted.
```
## Bandera
picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0}
## Notas adicionales
## Referencias
- https://guru99.es/string-charat-method-java/
