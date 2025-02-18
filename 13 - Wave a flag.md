Ondear una bandera
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

¿Puedes invocar indicadores de ayuda para una herramienta o un binario? Este programa tiene información extraordinariamente útil...

Pistas:
1.  Este programa solo funcionará en webshell o en otra computadora Linux.
2. Para que el archivo sea accesible en su shell, ingrese lo siguiente en el indicador de la Terminal:$ wget https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm
3. Ejecute este programa ingresando lo siguiente en el indicador de terminal: `$ ./warm`, pero primero tendrá que hacerlo ejecutable con`$ chmod +x warm`
4. -h y --help son los argumentos más comunes que se dan a los programas para obtener más información de ellos.
5. No todos los programas implementan funciones de ayuda como -h y --help.
* ==*Wget: descargar archivo*==
## Solución:
```
Siloy-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm
--2025-02-17 16:16:48--  https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm.3'

warm.3                       100%[=============================================>]  10.68K  --.-KB/s    in 0s      

2025-02-17 16:16:48 (301 MB/s) - 'warm.3' saved [10936/10936]

Siloy-picoctf@webshell:~$ chmod +x warm
Siloy-picoctf@webshell:~$ ./warm.3
-bash: ./warm.3: Permission denied
Siloy-picoctf@webshell:~$ ./warm  
Hello user! Pass me a -h to learn what I can do!
Siloy-picoctf@webshell:~$ -h
-bash: -h: command not found
Siloy-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
```
