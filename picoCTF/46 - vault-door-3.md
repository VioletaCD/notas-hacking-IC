# vault-door-3
## Descripcipción
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/a648ca6dd275b9454c5d0de6d0f6efd3/VaultDoor3.java)
## Pistas
- Make a table that contains each value of the loop variables and the corresponding buffer index that it writes to.
## Solucion
```
-- Haciendo uso de la consola de firefox
ejecutamos el siguiente código tomando como referencia parte del codigo otorgado por el reto

>>allow pasting
>>var password = "jU5t_a_sna_3lpm18gb41_u_4_mfr340"
>>var buffer = Array(32);
>>for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
>>console.log(buffer.join(''))
jU5t_a_s1mpl3_an4gr4m_4_u_1fb380

-----------------------------------------------------------------------------
comprobamos que la bandera es la correcta corriendo el codigo java
┌──(kali㉿kali)-[~/Documents/reversing/vaultdoor2]
└─$ javac VaultDoor3.java 
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
                                                                            
┌──(kali㉿kali)-[~/Documents/reversing/vaultdoor2]
└─$ java VaultDoor3      
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Enter vault password: picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_1fb380}
Access granted.
```
## Bandera
picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_1fb380}
## Notas adicionales
## Referencias
