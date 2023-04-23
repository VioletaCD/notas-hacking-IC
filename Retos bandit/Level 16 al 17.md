# Bandit Level 16 → Level 17

## Objetivo

Hay 2 archivos en el directorio de inicio: **passwords.old y passwords.new** . La contraseña para el siguiente nivel está en **passwords.new** y es la única línea que se ha cambiado entre **passwords.old y passwords.new**

**NOTA: si ha resuelto este nivel y ve '¡Adiós!' al intentar iniciar sesión en bandit18, esto está relacionado con el siguiente nivel, bandit19**

## Datos de acceso al nivel
- bandit16 
- JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solucion
```
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-03-18 21:03 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.0011s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.15 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Mar 18 13:02:16 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Mar 18 13:02:16 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Mar 18 13:01:16 2023 GMT; NotAfter: Mar 18 13:02:16 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEANFv2DANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMzE4MTMwMTE2WhcNMjMwMzE4MTMwMjE2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCz
oib9coqDepMGDv5LhLG2/g6ua6CdJiqGU5Tlv99/ioRCi5r+bj2S4AolVp+tYRTM
rZK615MaqNecsCwixQiR0VexpoTm04rGn+HVxFbSipSFPHM3ipzl2R6L6AYcsEVw
/FzqMyWBdILtTGd5EdStnuCjaOm5tH+ag4FgjVePA8TmYJMidlZkAtPJi+alTbE5
afioa5V/tx98LBPmimA+ttVOJiRLycyYbMxb+McuVRAsRzUAKsd3VcleBjlOMBzr
D4CzqbwSehq7gk+Q4MfLscJLXL525wLg00QhTDKw9hOLHtt1mw8BqrqrcSjXDpX/
uKj17knVBPHTT4oxzhpFAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQAz
hCjttAwIrlfyfbl7svgrl2Hyf5+9RVBNjllT9dX7FxOBGRHsjTjR7tFdia8tjhG+
axC94is+0ezMoqPrrC7ZFxEUKrKQiKWfmEJtSW3hR9GEGJatpTM6x0gudw7fIG3s
zGCNDr0XdHPESxC5TLjYoV3tb/jxQZMspIhoh8tjDfHmcMsy2bDWo1GcfPjCg9e8
EUQlXkJ6OiLLRIPGat9u7MNw1tneGCKtUZj7iU12Lbn01e/bYE6YYTael+Bo+Cpy
6hSfms3ZONYyHVRIjmZPDC+vfxRZ04F0dMuye8u/1DM6xPjKm1TAj5tQNGt9Yc9h
dW9VwBtx4Kc4JRty2Dkt
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 7B2B8BCDC21DF356B63AAAC9AE93F8BEFAA813C6C494346C5BB831E3BF993E22
    Session-ID-ctx:
    Resumption PSK: C4BEE48EE47DA133252845276EB300974AC3538A7EA21B049E0158ACC17F1345DC4FA807C05EEA2428EBF5B30DA02F3F
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - d7 0e d5 ed e8 fe fb fc-18 ba 46 36 22 af d1 1d   ..........F6"...
    0010 - aa d1 af 42 b5 a6 83 ed-aa 58 c0 39 aa ed 3f f4   ...B.....X.9..?.
    0020 - 40 dc 8b 0b 9d 23 50 8a-f0 57 be 64 14 c5 37 fb   @....#P..W.d..7.
    0030 - cf 75 00 85 f2 2a da ae-de 18 bd c9 9b b5 0a 39   .u...*.........9
    0040 - 48 a1 c5 f5 1b ea e7 07-98 c2 9e 68 a5 94 bd 8f   H..........h....
    0050 - df 52 f8 de be f3 3a e1-7f a3 62 21 e1 c4 dc b4   .R....:...b!....
    0060 - 05 05 b7 67 6c e0 8d 31-2d b2 e2 97 7c 7f 69 8e   ...gl..1-...|.i.
    0070 - d9 a8 ed d3 6e 32 43 94-95 b4 58 02 e6 ab b8 a1   ....n2C...X.....
    0080 - 37 42 9d 48 ff 08 65 13-1f 73 cf 9a 22 f1 47 82   7B.H..e..s..".G.
    0090 - bd a2 60 91 43 75 8a 1a-a6 d5 e5 32 f3 04 5d 39   ..`.Cu.....2..]9
    00a0 - 54 ee 5a 6c 87 dc bc b0-25 81 ee 3c 76 f4 d8 ce   T.Zl....%..<v...
    00b0 - 67 ca 1f 04 77 eb 27 90-19 e3 c2 43 1f 67 ac 04   g...w.'....C.g..
    00c0 - d9 cf 60 e3 52 c1 87 3a-6c 80 1b 7d 66 7c f7 1d   ..`.R..:l..}f|..

    Start Time: 1679173463
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 936EAC49291B493C42124861804DEDB0CA8CD122B88DF126DD9CECB9D0F4D3A7
    Session-ID-ctx:
    Resumption PSK: 237396DAD8ED050B792D2EDE88309A89848E4558E086B04ADEFC2BF0FC20A85DFC29E2081F43E540C44BE655A4A581B7
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - d7 0e d5 ed e8 fe fb fc-18 ba 46 36 22 af d1 1d   ..........F6"...
    0010 - ea 8a 2e 72 d5 2a 1e 9f-7c 62 81 3c ea ab 0e 63   ...r.*..|b.<...c
    0020 - 40 71 8e ce d6 eb fa 6d-a2 c2 5a 1f 91 01 ad 8a   @q.....m..Z.....
    0030 - dc 10 e7 d1 12 74 a4 f5-de 00 c1 68 0e 46 e9 1b   .....t.....h.F..
    0040 - b6 7c b7 bd 1a b8 a7 96-f3 81 ac c4 bf 1a 0e 98   .|..............
    0050 - 92 e5 cb e5 3d 2e 27 f8-d5 c7 5d 64 d4 18 de 66   ....=.'...]d...f
    0060 - f1 38 62 6c 98 c3 0c b9-23 58 89 49 2f e0 0f 34   .8bl....#X.I/..4
    0070 - 7d 7f 93 bc 99 d7 d8 e8-f8 e2 87 b1 e8 24 0a 81   }............$..
    0080 - ad 7b 5c 33 0f 7a 87 4f-21 64 79 ba e8 df 19 6a   .{\3.z.O!dy....j
    0090 - 17 eb 39 a0 51 72 eb 6a-2d b1 fe 16 2c 08 1c a3   ..9.Qr.j-...,...
    00a0 - 5b 4a 20 05 41 9d 31 44-2a 1f ef 84 fe 8a 1c fa   [J .A.1D*.......
    00b0 - 9a 88 f3 1d 5f a7 ea 94-19 ea fc 31 5e 46 12 40   ...._......1^F.@
    00c0 - 00 2d 12 11 99 62 01 38-62 cf b0 2c 7f 3f 33 4f   .-...b.8b..,.?3O

    Start Time: 1679173463
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$
exit

C:\Users\vayol\Documents>ssh -i llave1.txt bandit17@bandit.labs.overthewire.org -p2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames


      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

 Both python2 and python3 are installed.

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$
```

## Notas adicionales
Ejecutemos algunos escaneos para encontrar el servidor de escucha. Tenga en cuenta que netcat también puede realizar escaneos de puertos básicos. Es bueno saberlo porque muchos sistemas lo tienen predeterminado y es posible que se encuentre en una situación en la que no pueda usar nmap.
## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/
- https://keepcoding.io/blog/que-es-netcat/#:~:text=Netcat%20es%20una%20herramienta%20de,qu%C3%A9%20servicios%20se%20encuentran%20activos.
