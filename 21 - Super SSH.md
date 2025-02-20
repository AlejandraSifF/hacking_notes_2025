Using a Secure Shell (SSH) is going to be pretty important.

Additional details will be available after launching your challenge instance.

El uso de un Secure Shell (SSH) será bastante importante.

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.


Hints:
1. [https://linux.die.net/man/1/ssh](https://linux.die.net/man/1/ssh)
2. You can try logging in 'as' someone with `<user>`@titan.picoctf.net
3. How could you specify the port?
4. Remember, passwords are hidden when typed into the shell
Using a Secure Shell (SSH) is going to be pretty important.Can you `ssh` as `ctf-player` to `titan.picoctf.net` at port `64879` to get the flag?You'll also need the password `1ad5be0d`. If asked, accept the fingerprint with `yes`.If your device doesn't have a shell, you can use: [https://webshell.picoctf.org](https://webshell.picoctf.org/)If you're not sure what a shell is, check out our Primer: [https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)
## Solución
```
ssh: Could not resolve hostname ctf-player: Name or service not known
Siloy-picoctf@webshell:~$ ssh ctf-player titan.picoctf.net 64879
ssh: Could not resolve hostname ctf-player: Name or service not known
Siloy-picoctf@webshell:~$ ssh ctf-player@titan.picoctf.net -p 64879
The authenticity of host '[titan.picoctf.net]:64879 ([3.139.174.234]:64879)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:64879' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Permission denied, please try again.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_8306c99d}
Connection to titan.picoctf.net closed.
```

