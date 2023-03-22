# Bandit Level 15 → Level 16

## Objetivo

La contraseña para el siguiente nivel se puede recuperar enviando la contraseña del nivel actual al **puerto 30001 en localhost** usando encriptación SSL.

**Nota útil: ¿Obtienes "HEARTBEATING" y "Read R BLOCK"? Use -ign_eof y lea la sección "COMANDOS CONECTADOS" en la página de manual. Junto a 'R' y 'Q', el comando 'B' también funciona en esta versión de ese comando...**

## Datos de acceso al nivel
- bandit15 
- jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solucion
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
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
MIIDCzCCAfOgAwIBAgIEbWWPGjANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMzE4MTMwMTE2WhcNMjMwMzE4MTMwMjE2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCt
xNFVH+ItcDJOfoo8/Lg3QKyArUEnG6v08ctMIUBV7ZlgquQjAZLCfaXIf9C0D962
RSdI9Gp0CChuvdTAThOARwIWS5dCy3nRHSQ6oZDKPLi6MnQVzUtCFjb/mT2323iT
c15aIKXCVKmmA6dF2zaB5UVueiTFhu62lnMAg45c62cBGUaG3QFWi6nuD9NbADTZ
2vEr9hsmDkjBoj3OUBaOg1E9HPG27qmM9hIIdBAwfZOzMeIkRTPVfylHTgL1dROW
NW9V2xEljtDvIHoZI6wkfO32kmQYonO15tbEVTaPTjAJcajNGA+CSIWv90G6Ibfz
ERS+CKpem3VIqcb46+2rAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQA5
WAlRfVZomjI0M9RZmdM2NOwXX3zdS3CI3b+vNdcLpMbWw56dhxfw+j+QQObqoPx9
QBfi5wec4dKHrMo+yLrMiELwXDfRxDd55zdXhTmZbls5piJV+dk8mQuoBIbd3083
YZFkLdEKECcWP7F2z+78W3SA6iurlbgmGS3ic5X/XYFeuxuxfFLjaP0ZiVk3K13l
WmSui/Li3N8g9wOqzfWwpd0Sy+1RLUO0xO98eTkU9P2HBZScVi7ROe3z7zB4iSJE
ihLMk1kcqvBhMz98UcQ3fF44pUCJsF50BMpfh4a8aogRD9nESatTcQ8kkc6/VhE3
/0Sb0dqyb54fpMQDvkgU
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
    Session-ID: B03A194861EFDEC77BC531292E7C13929B7C8678720DFEB0E0E72F46035AE2E4
    Session-ID-ctx:
    Resumption PSK: B48BBE5E54CC6920608E259A17BA491E156A0BEBD877AB132091A829463C161949AA768110FCDD5AB9114C8C991234F6
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ab 9e e2 2d 85 da 95 51-2d ac ab 69 14 7e da b8   ...-...Q-..i.~..
    0010 - 6c 2d 8b f3 b4 d0 0f 00-1e b2 6d 34 dc 0d 2c bb   l-........m4..,.
    0020 - 3e e6 bd 41 c9 14 ec 5f-3c 14 dd d3 10 80 79 48   >..A..._<.....yH
    0030 - 2b cf 34 90 9a dd f3 cf-f5 38 24 70 b6 87 8d 15   +.4......8$p....
    0040 - 56 d7 f1 37 5c df 81 d0-eb 8c 5f 24 67 f8 f1 7d   V..7\....._$g..}
    0050 - 4a 2b 74 bc 15 7e 79 ee-23 f1 6c 21 3d 71 a4 ba   J+t..~y.#.l!=q..
    0060 - 64 a2 30 0b 71 5b 51 3d-eb bc 5a 47 f0 e3 f6 1e   d.0.q[Q=..ZG....
    0070 - c8 b4 61 bd 9a df dd 3f-5a 31 d5 96 e9 2d 04 8e   ..a....?Z1...-..
    0080 - 74 58 36 43 fa fa 52 01-99 c0 20 05 d4 4b 2e eb   tX6C..R... ..K..
    0090 - 32 18 c8 7d 09 8b c4 f6-ba a0 79 81 74 a1 45 80   2..}......y.t.E.
    00a0 - e2 6d 38 55 5a ff c8 c2-fe fd 81 f9 e5 18 87 7f   .m8UZ...........
    00b0 - 48 9e 83 20 58 7c 87 30-41 7e 15 4a d7 ae ce 70   H.. X|.0A~.J...p
    00c0 - 2a ee ba 5e af e2 1a 9a-da 97 a7 6d 8f f3 b6 b3   *..^.......m....

    Start Time: 1679172208
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
    Session-ID: AC4E9470847E0DC1B648033FCD991DC464D16314ED1097FC469B322AD72A1A8E
    Session-ID-ctx:
    Resumption PSK: B5BC577E4AAEA3BEF9E841C136C3D2CDF0F7F385047935A15717C7CDF51D2753D2E6CF964A6BDED57713AFFDF08CE318
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ab 9e e2 2d 85 da 95 51-2d ac ab 69 14 7e da b8   ...-...Q-..i.~..
    0010 - 49 87 ad 4c 26 50 1c 66-30 12 dd dc 32 78 f6 a8   I..L&P.f0...2x..
    0020 - 58 f7 70 30 e8 ef 92 c6-87 24 bb 49 8e 29 e5 fa   X.p0.....$.I.)..
    0030 - a9 91 7e cf 0f 87 71 34-6a ae 93 f6 c3 52 cb 6f   ..~...q4j....R.o
    0040 - 58 0b 38 9c da a4 2c 84-f9 9e 98 20 e7 81 7a 1d   X.8...,.... ..z.
    0050 - 3f 5f 33 9f 97 ab a9 cb-19 1b bf ec 47 92 83 5e   ?_3.........G..^
    0060 - 7a 3e 25 88 96 bf 2a 5e-4b 37 72 f0 c2 bd 59 4c   z>%...*^K7r...YL
    0070 - 33 47 43 50 e7 d9 f1 9e-bc af 80 fb 68 93 22 15   3GCP........h.".
    0080 - 99 b3 8c 0a e6 38 19 57-88 63 f9 c2 a0 d9 c8 b6   .....8.W.c......
    0090 - 93 a8 36 3e 9e 03 f0 9d-81 82 ef 7c 31 12 48 dd   ..6>.......|1.H.
    00a0 - 3a ae 1f ad b6 33 c8 18-4b 7e 31 35 b7 8f dc 3e   :....3..K~15...>
    00b0 - 01 8e 28 97 b9 df 74 50-c9 d4 b5 88 37 31 5a b2   ..(...tP....71Z.
    00c0 - dd 55 33 92 8a a2 48 81-09 7e 48 92 bd aa ff 18   .U3...H..~H.....

    Start Time: 1679172208
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$
```

## Notas adicionales

## Referencias
- https://rundata.wordpress.com/2013/03/21/overthewire-bandit-wargame-solutions-1-24/
- https://www.globalsign.com/es/centro-de-informacion-ssl/que-es-ssl
