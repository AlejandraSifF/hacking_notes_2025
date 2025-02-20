### arreglame1.py
#### Description

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
Corrija el error de sintaxis en este script de Python para imprimir la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/25/fixme1.py)

Hints:
1. Indentation is very meaningful in Python
2. To view the file in the webshell, do: `$ nano fixme1.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 

```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2025-02-20 04:27:00--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.92, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                    100%[=============================================>]     837  --.-KB/s    in 0s      

2025-02-20 04:27:01 (368 MB/s) - 'fixme1.py' saved [837/837]

Siloy-picoctf@webshell:~$ nano fixme1.py
Siloy-picoctf@webshell:~$ nano fixme1.py
Siloy-picoctf@webshell:~$ cat ^C
Siloy-picoctf@webshell:~$ cat fixme1    
cat: fixme1: No such file or directory
Siloy-picoctf@webshell:~$ python fixme1
python: can't open file '/home/Siloy-picoctf/fixme1': [Errno 2] No such file or directory
Siloy-picoctf@webshell:~$ python fixme1
python: can't open file '/home/Siloy-picoctf/fixme1': [Errno 2] No such file or directory
Siloy-picoctf@webshell:~$ nano fixme1.py
Siloy-picoctf@webshell:~$ python fixme1
python: can't open file '/home/Siloy-picoctf/fixme1': [Errno 2] No such file or directory
Siloy-picoctf@webshell:~$ nano fixme1.py
Siloy-picoctf@webshell:~$ nano fixme1.py
Siloy-picoctf@webshell:~$ nano fixme1.py
Siloy-picoctf@webshell:~$ python3 fixme1.py
  File "/home/Siloy-picoctf/fixme1.py", line 13
    print("u")
TabError: inconsistent use of tabs and spaces in indentation
Siloy-picoctf@webshell:~$ nano fixme1.py
Siloy-picoctf@webshell:~$ python3 fixme1.py
  File "/home/Siloy-picoctf/fixme1.py", line 13
    print(i)        
TabError: inconsistent use of tabs and spaces in indentation
Siloy-picoctf@webshell:~$ nano fixme1.py
Siloy-picoctf@webshell:~$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```
