Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `b60940ca`

Additional details will be available after launching your challenge instance.
¿Sabes cómo moverte entre directorios y leer archivos en el shell? Inicia el contenedor, hazle un ssh y luego haz un sls una vez conectado para comenzar. Inicia sesión a través de ssh como ctf-player con la contraseña b60940ca

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

Consejos / Hints:
1. Finding a cheatsheet for bash would be really helpful!
CHALLENGE ENDPOINTS
SSH	ssh ctf-player@venus.picoctf.net -p 52922

## Solución
```

Siloy-picoctf@webshell:~$ ssh ctf-player@venus.picoctf.net -p 52922
ctf-player@venus.picoctf.net's password: 
Permission denied, please try again.
ctf-player@venus.picoctf.net's password: 
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-1041-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Mon Feb 17 16:59:07 2025 from 127.0.0.1
ctf-player@pico-chall$ ls]
-bash: ls]: command not found
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt
c1754242}
ctf-player@pico-chall$ cd..
-bash: cd..: command not found
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls
ctf-player
ctf-player@pico-chall$ ls
ctf-player
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls
2of3.flag.txt  boot  etc   instructions-to-3of3.txt  lib64  mnt  proc  run   srv  tmp  var
bin            dev   home  lib                       media  opt  root  sbin  sys  usr
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ Connection to venus.picoctf.net closed by remote host.
Connection to venus.picoctf.net closed.
Siloy-picoctf@webshell:~$ 

Contraseña: picoCTF{xxsh_0ut_0f_\/\/4t3r_c1754242}
```
