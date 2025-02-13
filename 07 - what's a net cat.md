Using netcat (nc) is going to be pretty important. Can you connect to jupiter.challenges.picoctf.org at port 41120 to get the flag?

El uso de netcat (nc) será muy importante. ¿Puedes conectarte a jupiter.challenges.picoctf.orgese puerto 41120para obtener la bandera?

Pista:
1. nc [tutorial](https://linux.die.net/man/1/nc)
La utilidad **nc** (o **netcat** ) se utiliza para casi cualquier cosa que involucre TCP o UDP. Puede abrir conexiones TCP, enviar paquetes UDP, escuchar en puertos TCP y UDP arbitrarios, realizar escaneo de puertos y manejar tanto IPv4 como IPv6. A diferencia de **[telnet](https://linux.die.net/man/1/telnet)** (1), **nc** ejecuta scripts de manera elegante y separa los mensajes de error en el error estándar en lugar de enviarlos a la salida estándar, como hace **[telnet](https://linux.die.net/man/1/telnet)** (1) con algunos.

```
"Comunicación entre 2 computadoras"
```


## Solución 
```
Siloy-picoctf@webshell:~$ nc  jupiter.challenges.picoctf.org 41120
You're on your way to becoming the net cat master

picoCTF{nEtCat_Mast3ry_3214be47}
```