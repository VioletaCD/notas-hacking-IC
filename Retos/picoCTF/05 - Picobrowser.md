# Dont-use-client-side
## Descripcipción
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/26704/` ([link](https://jupiter.challenges.picoctf.org/problem/26704/)) or http://jupiter.challenges.picoctf.org:26704
## Pistas
- Never trust the client
## Solucion
```
- DESDE CONSOLA
rojiblanca-picoctf@webshell:~$ curl -s https://jupiter.challenges.picoctf.org/problem/26704/flag -H "User-Agent: picobrowser" | grep pico
         <!-- <strong>Title</strong> --> picobrowser!
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0}</code></p>
rojiblanca-picoctf@webshell:~$ 
```
## Bandera
picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0
## Notas adicionales
## Referencias
