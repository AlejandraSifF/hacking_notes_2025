Plomería 
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.

A veces es necesario manejar datos de procesos fuera de un archivo. ¿Puedes encontrar una forma de conservar la salida de este programa y buscar la bandera? Conéctate a `jupiter.challenges.picoctf.org 14291`

Pistas:
1. Remember the flag format is picoCTF{XXXX}
2. What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)

## Solución 
Conectar en netcat y buscar la salida en un archivo, luego buscar la bandera 
```
Siloy-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 > salida
^C
Siloy-picoctf@webshell:~$ cat salida | grep pico
picoCTF{digital_plumb3r_ea8bfec7}
Siloy-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 | grep pico
picoCTF{digital_plumb3r_ea8bfec7}
```
