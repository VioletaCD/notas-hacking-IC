# Dont-use-client-side
## Descripcipción
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/37821/` ([link](https://jupiter.challenges.picoctf.org/problem/37821/)) or http://jupiter.challenges.picoctf.org:37821
## Pistas
- Never trust the client
## Solucion
```
Se soluciona siguiendo el orden de los if encontrados en el codigo de la pagina web
se arma uno a uno en un editor de textos y se obtiene la bandera
 function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == 'a3c8') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_1') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == '9}') {
                  alert("Password Verified")
                  }
        
picoCTF{no_clients_plz_1a3c89}
```
## Bandera
picoCTF{no_clients_plz_1a3c89}
## Notas adicionales
## Referencias
