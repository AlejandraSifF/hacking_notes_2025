#### Description

Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.

Additional details will be available after launching your challenge instance.
  
¿Los usuarios avanzados no se cansan de cometer errores ortográficos en el shell? ¡Ya no! Presentamos Special, la interfaz de corrección ortográfica para Linux. Ahora, cada palabra está escrita y capitalizada correctamente... ¡automáticamente y en segundo plano! Sea el primero en probar Special en versión beta y no dude en contarnos todo sobre cómo Special agiliza cada proceso de desarrollo al que se enfrenta. Cuando sus compañeros de trabajo vean su increíble interfaz de shell, dígales: Eso es Special (TM)Inicie su instancia para ver los detalles de la conexión.

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

Start your instance to see connection details.`ssh -p 62781 ctf-player@saturn.picoctf.net`The password is `3f39b042`
## Solución 
```
Siloy-picoctf@webshell:~$ ssh -p 62781 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:62781 ([13.59.203.175]:62781)' can't be established.
ED25519 key fingerprint is SHA256:tJ0wuU5yBvNO/FrkHmR9iY36VJClMhKV+Hq2sxqKFmg.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:62781' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

Special$ ls
Is 
sh: 1: Is: not found
Special$ Clear & find .
Clear & find . 
sh: 1: Clear: not found
.
./blargh
./blargh/flag.txt
./.cache
./.cache/motd.legal-displayed
Special$ cat ./blargh/flag.txt
Cat ./blargh/flag.txt 
sh: 1: Cat: not found
Special$ Clear &  cat ./blargh/flag.txt
Clear & cat ./blargh/flag.txt 
sh: 1: Clear: not found
picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}Special$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
Siloy-picoctf@webshell:~$ 
```
