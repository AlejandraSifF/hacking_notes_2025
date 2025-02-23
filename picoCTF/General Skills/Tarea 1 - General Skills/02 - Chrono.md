* Crono
#### Description

How to automate tasks to run at intervals on linux servers?

Additional details will be available after launching your challenge instance.

  
¿Cómo automatizar tareas para que se ejecuten a intervalos en servidores Linux?

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.
```
Server: saturn.picoctf.net
Port: 59227
Username: picoplayer 
Password: bLgSMmbY6X
```


## Solución 
```
Siloy-picoctf@webshell:~$ ssh -p 59227 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Sun Feb 23 04:14:18 2025 from 3.140.102.47
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1b4d8744}
picoplayer@challenge:~$ ^C
picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
Siloy-picoctf@webshell:~$ 
```
