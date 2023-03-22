# money-ware
## Descripcipción
Flag format: picoCTF{Malwarename} The first letter of the malware name should be capitalized and the rest lowercase. Your friend just got hacked and has been asked to pay some bitcoins to `1Mz7153HMuxXTuR2R1t78mGSdzaAtNbBWX`. He doesn’t seem to understand what is going on and asks you for advice. Can you identify what malware he’s being a victim of?
## Pistas
- Some crypto-currencies abuse databases exist; check them out!
-  Maybe Google might help.
## Solucion
```
-se ingresa un usuario cualquiera y da acceso, misma que genera un token en las cookies
-El token dentro de kali-linux se guarda en un txt
-En la consola de Kali se ejecuta lo siguiente
──(kali㉿kali)-[~]
└─$ john token
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 2 OpenMP threads
Proceeding with single, rules:Single
Press 'q' or Ctrl-C to abort, almost any other key for status
Almost done: Processing the remaining buffered candidate passwords, if any.
Proceeding with wordlist:/usr/share/john/password.lst
Proceeding with incremental:ASCII
0g 0:00:01:02  3/3 0g/s 2869Kp/s 2869Kc/s 2869KC/s pak5kk..pol2eu
Session aborted
                                                                             
┌──(kali㉿kali)-[~]
└─$ cd /usr/share/wordlists 
                                                                             
┌──(kali㉿kali)-[/usr/share/wordlists]
└─$ ls -la
total 52124
drwxr-xr-x   2 root root     4096 Mar  9 01:01 .
drwxr-xr-x 347 root root    12288 Mar  9 00:59 ..
lrwxrwxrwx   1 root root       26 Mar  9 01:01 amass -> /usr/share/amass/wordlists
lrwxrwxrwx   1 root root       25 Mar  9 01:01 dirb -> /usr/share/dirb/wordlists
lrwxrwxrwx   1 root root       30 Mar  9 01:01 dirbuster -> /usr/share/dirbuster/wordlists                                                                
lrwxrwxrwx   1 root root       41 Mar  9 01:01 fasttrack.txt -> /usr/share/set/src/fasttrack/wordlist.txt
lrwxrwxrwx   1 root root       45 Mar  9 01:01 fern-wifi -> /usr/share/fern-wifi-cracker/extras/wordlists
lrwxrwxrwx   1 root root       28 Mar  9 01:01 john.lst -> /usr/share/john/password.lst
lrwxrwxrwx   1 root root       27 Mar  9 01:01 legion -> /usr/share/legion/wordlists                                                                      
lrwxrwxrwx   1 root root       46 Mar  9 01:01 metasploit -> /usr/share/metasploit-framework/data/wordlists
lrwxrwxrwx   1 root root       41 Mar  9 01:01 nmap.lst -> /usr/share/nmap/nselib/data/passwords.lst
-rw-r--r--   1 root root 53357329 Feb 16 13:34 rockyou.txt.gz
lrwxrwxrwx   1 root root       39 Mar  9 01:01 sqlmap.txt -> /usr/share/sqlmap/data/txt/wordlist.txt
lrwxrwxrwx   1 root root       25 Mar  9 01:01 wfuzz -> /usr/share/wfuzz/wordlist                                                                         
lrwxrwxrwx   1 root root       37 Mar  9 01:01 wifite.txt -> /usr/share/dict/wordlist-probable.txt
                                                                             
┌──(kali㉿kali)-[/usr/share/wordlists]
└─$ sudo gzip -d rockyou.txt.gz
[sudo] password for kali: 
                                                                             
┌──(kali㉿kali)-[/usr/share/wordlists]
└─$ ls -lah
total 134M
drwxr-xr-x   2 root root 4.0K Mar 14 14:57 .
drwxr-xr-x 347 root root  12K Mar  9 00:59 ..
lrwxrwxrwx   1 root root   26 Mar  9 01:01 amass -> /usr/share/amass/wordlists                                                                            
lrwxrwxrwx   1 root root   25 Mar  9 01:01 dirb -> /usr/share/dirb/wordlists
lrwxrwxrwx   1 root root   30 Mar  9 01:01 dirbuster -> /usr/share/dirbuster/wordlists                                                                    
lrwxrwxrwx   1 root root   41 Mar  9 01:01 fasttrack.txt -> /usr/share/set/src/fasttrack/wordlist.txt
lrwxrwxrwx   1 root root   45 Mar  9 01:01 fern-wifi -> /usr/share/fern-wifi-cracker/extras/wordlists                                                     
lrwxrwxrwx   1 root root   28 Mar  9 01:01 john.lst -> /usr/share/john/password.lst
lrwxrwxrwx   1 root root   27 Mar  9 01:01 legion -> /usr/share/legion/wordlists                                                                          
lrwxrwxrwx   1 root root   46 Mar  9 01:01 metasploit -> /usr/share/metasploit-framework/data/wordlists
lrwxrwxrwx   1 root root   41 Mar  9 01:01 nmap.lst -> /usr/share/nmap/nselib/data/passwords.lst
-rw-r--r--   1 root root 134M Feb 16 13:34 rockyou.txt
lrwxrwxrwx   1 root root   39 Mar  9 01:01 sqlmap.txt -> /usr/share/sqlmap/data/txt/wordlist.txt
lrwxrwxrwx   1 root root   25 Mar  9 01:01 wfuzz -> /usr/share/wfuzz/wordlist
lrwxrwxrwx   1 root root   37 Mar  9 01:01 wifite.txt -> /usr/share/dict/wordlist-probable.txt
                                                                             
┌──(kali㉿kali)-[/usr/share/wordlists]
└─$ head rockyou.txt
123456
12345
123456789
password
iloveyou
princess
1234567
rockyou
12345678
abc123
                                                                             
┌──(kali㉿kali)-[/usr/share/wordlists]
└─$ cd                     
                                                                             
┌──(kali㉿kali)-[~]
└─$ ls     
Desktop    Downloads  Music     Public     token
Documents  haking     Pictures  Templates  Videos
                                                                             
┌──(kali㉿kali)-[~]
└─$ john token -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:02 DONE (2023-03-14 14:59) 0.4048g/s 2994Kp/s 2994Kc/s 2994KC/s iloverob4live345..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 

en la pestaña debuger de https://jwt.io/
-se ingresa el token dado por las cookies
-se cambia el payload por la palabra "admin"
-y se agrega la palabra dada por el kali 
-se modifica el token
-se recetea la pagina y se obtiene la bandera

picoCTF{jawt_was_just_what_you_thought_f859ab2f}
```
## Bandera
picoCTF{jawt_was_just_what_you_thought_f859ab2f}
## Notas adicionales
Este _Ransomware_ infecta equipos a través archivos de Microsoft Office maliciosos y se propaga a otros
## Referencias
https://jwt.io/
https://es.wikipedia.org/wiki/JSON_Web_Token
https://github.com/openwall/john
