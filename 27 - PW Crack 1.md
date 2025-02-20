#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.

Hints:
1.  To view the file in the webshell, do: `$ nano level1.py`
2. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
3. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 
```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.py
--2025-02-20 04:49:24--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                    100%[=============================================>]     876  --.-KB/s    in 0s      

2025-02-20 04:49:24 (60.1 MB/s) - 'level1.py' saved [876/876]

Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
--2025-02-20 04:49:36--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc          100%[=============================================>]      30  --.-KB/s    in 0s      

2025-02-20 04:49:37 (2.19 MB/s) - 'level1.flag.txt.enc' saved [30/30]

Siloy-picoctf@webshell:~$ nano level1.py
Siloy-picoctf@webshell:~$ cat ^C
Siloy-picoctf@webshell:~$ cat level1.flag.txt.enc
[gE]__TgS^S

           JSiloy-picoctf@webshell:~$ ^C
Siloy-picoctf@webshell:~$ cat level1.flag.txt.enc
[gE]__TgS^S

           JSiloy-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: [gE]__TgS^S
That password is incorrect
Siloy-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: [gE]__TgS^S

           JThat password is incorrect
Siloy-picoctf@webshell:~$ 
Siloy-picoctf@webshell:~$ nano level1.py
Siloy-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
```
