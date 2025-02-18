Cremallera grande

Unzip this archive and find the flag.
Download zip file

Hints:
1. Can grep be instructed to look at every file in a directory and its subdirectories?

## Solución

```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/505/big-zip-files.zip
--2025-02-17 18:01:56--  https://artifacts.picoctf.net/c/505/big-zip-files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3182988 (3.0M) [application/octet-stream]
Saving to: 'big-zip-files.zip.2'

big-zip-files.zip.2          100%[=============================================>]   3.04M  1.82MB/s    in 1.7s    

2025-02-17 18:01:58 (1.82 MB/s) - 'big-zip-files.zip.2' saved [3182988/3182988]

Siloy-picoctf@webshell:~$ unzip big-zip-files.zip
.
.
.
.
.
.
.
.
.
.
Siloy-picoctf@webshell:~$ grep -r pico
README.txt:Welcome to the picoCTF webshell!
README.txt:picoCTF challenges.
README.txt:other@picoctf.org and we will consider adding it.
README.txt:  Extensive brute-forcing is not necessary to solve picoCTF challenges.
README.txt:- If you change your username through the picoCTF website, you will
.python_history:'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
.python_history:nc jupiter.challenges.picoctf.org 29956
file:picoCTF{grep_is_good_to_find_things_5af9d829}
.wget-hsts:mercury.picoctf.net  0       0       1739385835      0
flag:picoCTF{s4n1ty_v3r1f13d_2aa22101}
salida:picoCTF{digital_plumb3r_ea8bfec7}
.bash_history:nc  jupiter.challenges.picoctf.org 41120
.bash_history:nc jupiter.challenges.picoctf.org 14291 
.bash_history:nc jupiter.challenges.picoctf.org 14291 > salida
.bash_history:cat salida | grep pico
.bash_history:nc jupiter.challenges.picoctf.org 14291 | grep pico
.bash_history:nc saturn.picoctf.net 58582
.bash_history:$ nc mercury.picoctf.net 22902
.bash_history:nc mercury.picoctf.net 22902
grep: strings: binary file matches
grep: warm: binary file matches
grep: warm.1: binary file matches
grep: warm.2: binary file matches
grep: warm.3: binary file matches
grep: static: binary file matches
grep: static.1: binary file matches
grep: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet: binary file matches
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
Siloy-picoctf@webshell:~$ 
```