#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución 
```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py
--2025-02-20 05:10:36--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                    100%[=============================================>]   1.31K  --.-KB/s    in 0s      

2025-02-20 05:10:36 (93.8 MB/s) - 'level3.py' saved [1337/1337]

Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2025-02-20 05:10:54--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc          100%[=============================================>]      31  --.-KB/s    in 0s      

2025-02-20 05:10:54 (2.67 MB/s) - 'level3.flag.txt.enc' saved [31/31]

Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
--2025-02-20 05:11:11--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin              100%[=============================================>]      16  --.-KB/s    in 0s      

2025-02-20 05:11:11 (1.10 MB/s) - 'level3.hash.bin' saved [16/16]

Siloy-picoctf@webshell:~$ bvi level3.hash.bin

[1]+  Stopped                 bvi level3.hash.bin
Siloy-picoctf@webshell:~$ nano level3.py
Siloy-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```