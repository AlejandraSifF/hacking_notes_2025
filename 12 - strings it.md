Can you find the flag in file without running it?
¿Puedes encontrar la bandera en el archivo sin ejecutarlo?

Pistas:
1. [instrumentos de cuerda](https://linux.die.net/man/1/strings)

* ==Para sustraer las cadenas strings: strings strings | grep pico== 
## Solución
```
Siloy-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
--2025-02-17 16:04:20--  https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                                    100%[=======================================================================================================================================>] 757.84K  1.85MB/s    in 0.4s  

Siloy-picoctf@webshell:~$ strings strings | grep pico 
picoCTF{5tRIng5_1T_d66c7bb7}

```
