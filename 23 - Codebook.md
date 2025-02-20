### Libro de códigos
#### Description

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt) 
Ejecute el script de Python `code.py`en el mismo directorio que `codebook.txt`.

- [Descargar código.py](https://artifacts.picoctf.net/c/1/code.py)
- [Descargar libro de códigos.txt](https://artifacts.picoctf.net/c/1/codebook.txt)


Hints:
1.  On the webshell, use `ls` to see if both files are in the directory you are in
2. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución:
```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/code.py
--2025-02-20 04:01:06--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                      100%[=============================================>]   1.25K  --.-KB/s    in 0s      

2025-02-20 04:01:06 (4.67 MB/s) - 'code.py' saved [1278/1278]

Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2025-02-20 04:01:26--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                 100%[=============================================>]      27  --.-KB/s    in 0s      

2025-02-20 04:01:26 (255 KB/s) - 'codebook.txt' saved [27/27]

Siloy-picoctf@webshell:~$ ls
README.txt  code.py  codebook.txt  runme.py
Siloy-picoctf@webshell:~$  code.py
-bash: code.py: command not found
Siloy-picoctf@webshell:~$ str_xor  code.py
-bash: str_xor: command not found
Siloy-picoctf@webshell:~$ cat  code.py

import random
import sys



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x13) + chr(0x01) + chr(0x17) + chr(0x07) + chr(0x2c) + chr(0x3a) + chr(0x2f) + chr(0x1a) + chr(0x0d) + chr(0x53) + chr(0x0c) + chr(0x47) + chr(0x0a) + chr(0x5f) + chr(0x5e) + chr(0x02) + chr(0x3e) + chr(0x5a) + chr(0x56) + chr(0x5d) + chr(0x45) + chr(0x5d) + chr(0x58) + chr(0x31) + chr(0x0d) + chr(0x58) + chr(0x0f) + chr(0x02) + chr(0x5a) + chr(0x10) + chr(0x0e) + chr(0x5d) + chr(0x13)



def print_flag():
  try:
    codebook = open('codebook.txt', 'r').read()
    
    password = codebook[4] + codebook[14] + codebook[13] + codebook[14] +\
               codebook[23]+ codebook[25] + codebook[16] + codebook[0]  +\
               codebook[25]
               
    flag = str_xor(flag_enc, password)
    print(flag)
  except FileNotFoundError:
    print('Couldn\'t find codebook.txt. Did you download that file into the same directory as this script?')



def main():
  print_flag()



if __name__ == "__main__":
  main()

Siloy-picoctf@webshell:~$ cat codebook.txt
azbycxdwevfugthsirjqkplomn
Siloy-picoctf@webshell:~$ python code.py
picoCTF{c0d3b00k_455157_d9aa2df2}

```
