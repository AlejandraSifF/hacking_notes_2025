#### Description

Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.

Additional details will be available after launching your challenge instance.

ssh -p 54903 ctf-player@saturn.picoctf.net. The password is d8819d45
#### Consejos:
1.  What programs do you have access to?

#### Terminal de linux:
```
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/10-Specialer$ ssh -p 54903 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:54903 ([13.59.203.175]:54903)' can't be established.
ECDSA key fingerprint is SHA256:dJtvF/J5LfkJcePCA5aEPg1zZbM6yb37NnsNhGVyygI.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:54903,[13.59.203.175]:54903' (ECDSA) to the list of known hosts.
ctf-player@saturn.picoctf.net's password:
Specialer$
!          cd         else       hash       pwd        times
./         command    enable     help       read       trap
:          compgen    esac       history    readarray  true
[          complete   eval       if         readonly   type
[[         compopt    exec       in         return     typeset
]]         continue   exit       jobs       select     ulimit
alias      coproc     export     kill       set        umask
bash       declare    false      let        shift      unalias
bg         dirs       fc         local      shopt      unset
bind       disown     fg         logout     source     until
break      do         fi         mapfile    suspend    wait
builtin    done       for        popd       test       while
caller     echo       function   printf     then       {
case       elif       getopts    pushd      time       }
Specialer$ cd ../..
Specialer$ cd ../../
Specialer$ cd ../..
bin/   home/  lib/   lib64/
Specialer$ cd ../../
bin/   home/  lib/   lib64/
Specialer$ cd ../../home/ctf-player/
Specialer$ cd ctf-player
-bash: cd: ctf-player: No such file or directory
Specialer$ cd ctf-player/
-bash: cd: ctf-player/: No such file or directory
Specialer$ cd ../../home
Specialer$ pwd
/home
Specialer$ cd ctf-player/
Specialer$ cd ctf-player/
-bash: cd: ctf-player/: No such file or directory
Specialer$ echo $(<cadabra.txt)
-bash: cadabra.txt: No such file or directory

Specialer$ cd abra/
Specialer$ echo $(<cadabra.txt)
Nothing up my sleeve!
Specialer$ echo $(<cadaniel.txt)echo $(<cadaniel.txt)
Yes, I did it! I really did it! I'm a true wizard!echo Yes, I did it! I really did it! I'm a true wizard!
Specialer$ cd ../ala
Specialer$ echo $(<kazam.txt)
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_c42168d9}
Specialer$ Connection to saturn.picoctf.net closed by remote host.
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/10-Specialeyoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/10-Specialer$
```

## Solución:
```
picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_c42168d9}
```