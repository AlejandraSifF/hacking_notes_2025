#### Description

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)
Ejecute el script de Python y convierta el número dado de decimal a binario para obtener la bandera.[Descargar script de Python](https://artifacts.picoctf.net/c/23/convertme.py)

Hints:
1.  Type everything after the dollar sign in the webshell: $ wget , then paste the link after the space after wget and press enter. This will download the script for you in the webshell so you can run it!
2. The `str_xor` function does not need to be reverse engineered for this challenge.
3. If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
4. To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
5. Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
6. Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 convertme.py`

## Solución 
```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/convertme.py
--2025-02-20 04:15:54--  https://artifacts.picoctf.net/c/23/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                 100%[=============================================>]   1.16K  --.-KB/s    in 0s      

2025-02-20 04:15:54 (1010 MB/s) - 'convertme.py' saved [1189/1189]

Siloy-picoctf@webshell:~$ python3 convertme.py
If 29 is in decimal base, what is it in binary base?
Answer: 0001 1101
That isn't a binary number. Binary numbers contain only 1's and 0's
Siloy-picoctf@webshell:~$ python3 convertme.py
If 20 is in decimal base, what is it in binary base?
Answer: 00110101 00110000 00100000 00110101 00110111
That isn't a binary number. Binary numbers contain only 1's and 0's
Siloy-picoctf@webshell:~$ python3 convertme.py
If 90 is in decimal base, what is it in binary base?
Answer: 00111001 00110000
That isn't a binary number. Binary numbers contain only 1's and 0's
Siloy-picoctf@webshell:~$ python3 convertme.py
If 52 is in decimal base, what is it in binary base?
Answer: 0011 0100
That isn't a binary number. Binary numbers contain only 1's and 0's
Siloy-picoctf@webshell:~$ python3 convertme.py
If 42 is in decimal base, what is it in binary base?
Answer: 0010 1010
That isn't a binary number. Binary numbers contain only 1's and 0's
Siloy-picoctf@webshell:~$ python3 convertme.py
If 41 is in decimal base, what is it in binary base?
Answer: 41
That isn't a binary number. Binary numbers contain only 1's and 0's
Siloy-picoctf@webshell:~$ python3 convertme.py
If 62 is in decimal base, what is it in binary base?
Answer: 111110
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
```
