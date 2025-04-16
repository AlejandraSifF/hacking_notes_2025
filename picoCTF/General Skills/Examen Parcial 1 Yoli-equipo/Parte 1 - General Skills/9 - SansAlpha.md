#### Description

The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.

Additional details will be available after launching your challenge instance.

`ssh -p 54221 ctf-player@mimas.picoctf.net`Use password: `1ad5be0d`

#### Consejos:
1.  Where can you get some letters?

usar la terminal es usando [[Wildcards]] y números:
```
ctf-player@mimas.picoctf.net
ssh: Could not resolve hostname mimas.picoctf.net: No address associated with hostname
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/9-SansAlpha$ ssh -p 54221 ctf-player@mimas.picoctf.net
The authenticity of host '[mimas.picoctf.net]:54221 ([52.15.88.75]:54221)' can't be established.
ECDSA key fingerprint is SHA256:5rS4L0YbD+igsLhyOOBACWOhhxzoxbv5MOee+i2HKSg.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[mimas.picoctf.net]:54221,[52.15.88.75]:54221' (ECDSA) to the list of known hosts.
ctf-player@mimas.picoctf.net's password:
Permission denied, please try again.
ctf-player@mimas.picoctf.net's password:
Permission denied, please try again.
ctf-player@mimas.picoctf.net's password:
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

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

SansAlpha$ ls -la
SansAlpha: Unknown character detected
SansAlpha$ */*
bash: blargh/flag.txt: Permission denied

SansAlpha$ /*/??????
/bin/base32: extra operand ‘/bin/base64’
Try '/bin/base32 --help' for more information.

SansAlpha$ /*/????64 */*
/bin/base64: extra operand ‘/bin/x86_64’
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */*
/bin/base64: extra operand ‘blargh/flag.txt’
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV83NzVhYzEyZH0=

SansAlpha$ echo cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV83NzVhYzEyZH0=
SansAlpha: Unknown character detected
SansAlpha$ echo cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV83NzVhYzEyZH0= | base64 -d
SansAlpha: Unknown character detected
SansAlpha$ echo cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV83NzVhYzEyZH0= | base64 -d
SansAlpha: Unknown character detected
SansAlpha$  Connection to mimas.picoctf.net closed by remote host.
Connection to mimas.picoctf.net closed.

```

* Ayudándonos de Cyberchef:
  ![[Pasted image 20250415132057.png]]


## Solución:
```
picoCTF{7h15_mu171v3r53_15_m4dn355_775ac12d}
```

## Referencias:
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y21WMGRYSnVJREFnY0dsamIwTlVSbnMzYURFMVgyMTFNVGN4ZGpOeU5UTmZNVFZmYlRSa2JqTTFOVjgzTnpWaFl6RXlaSDA9
