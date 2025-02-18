Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip
El uso de tabcomplete en la Terminal agregará años a su vida, especialmente cuando se trata de estructuras de directorios y nombres de archivos largos y confusos: Addadshashanammu.zip

Hints / Consejos:
1. After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...
Después de descomprimir, este problema se puede solucionar presionando 11 botones (principalmente Tab)...    ---> **Thissssss**

* *==Era dar Tabulación 11 veces==* 
## Solución 
```
Siloy-picoctf@webshell:~$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
replace Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet? [y]es, [n]o, [A]ll, [N]one, [r]ename: r
new name: ^CSiloy-picoctf@webshell:~$ 
Siloy-picoctf@webshell:~$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
replace Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet? [y]es, [n]o, [A]ll, [N]one, [r]ename: y
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
Siloy-picoctf@webshell:~$ ls
Addadshashanammu      README.txt  flag      grep.php.1  static    strings  warm.1  warm.3
Addadshashanammu.zip  file        grep.php  salida      static.1  warm     warm.2
Siloy-picoctf@webshell:~$ cd Addadshashanammu.zip
-bash: cd: Addadshashanammu.zip: Not a directory
Siloy-picoctf@webshell:~$ cd file
-bash: cd: file: Not a directory
Siloy-picoctf@webshell:~$ cd Addadshashanammu    
Siloy-picoctf@webshell:~/Addadshashanammu$ ls
Almurbalarammi
Siloy-picoctf@webshell:~/Addadshashanammu$ ls
Almurbalarammi
Siloy-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi$ ls
Ashalmimilkala
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi$ cd Ashalmimilkala/
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi/
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ ls
Maelkashishi
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ cd Maelkashishi/
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi$ ls
Onnissiralis
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi$ cd Onnissiralis/
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ 
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ 
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ 
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ 
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ 
ls
Ularradallaku
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ 
cd Ularradallaku/
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/U
larradallaku$ ls
fang-of-haynekhtnamet
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/U
larradallaku$ file fang-of-haynekhtnamet
fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=72a56ba85df661b5a985999a435927c01095cccf, not stripped
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/U
larradallaku$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}
Siloy-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/U
larradallaku$ 
```
