This file has a flag in plain sight (aka "in-the-clear").
Este archivo tiene una bandera a simple vista (también conocida como "sin trabas"). Descargar bandera .

Pistas:
1. Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
3. $ man cat
## Solución
Descargar el archivo y hacerle cat
```
Siloy-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag           
--2025-02-12 18:43:55--  https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                         100%[=============================================>]      34  --.-KB/s    in 0s      

2025-02-12 18:43:55 (14.6 MB/s) - 'flag' saved [34/34]

Siloy-picoctf@webshell:~$ cat flag

picoCTF{s4n1ty_v3r1f13d_2aa22101}
```