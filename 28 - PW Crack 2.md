Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.

## Solución
```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py
--2025-02-20 04:58:03--  https://artifacts.picoctf.net/c/15/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                    100%[=============================================>]     914  --.-KB/s    in 0s      

2025-02-20 04:58:03 (39.0 MB/s) - 'level2.py' saved [914/914]

Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
--2025-02-20 04:58:17--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc          100%[=============================================>]      31  --.-KB/s    in 0s      

2025-02-20 04:58:17 (1.62 MB/s) - 'level2.flag.txt.enc' saved [31/31]

Siloy-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: 2222
That password is incorrect
Siloy-picoctf@webshell:~$ nano level2.py
Siloy-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: 545799101
That password is incorrect
Siloy-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: 4ec9
That password is incorrect
Siloy-picoctf@webshell:~$ nano level2.py
Siloy-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: !'?A
That password is incorrect
Siloy-picoctf@webshell:~$ nano level2.py
Siloy-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```
