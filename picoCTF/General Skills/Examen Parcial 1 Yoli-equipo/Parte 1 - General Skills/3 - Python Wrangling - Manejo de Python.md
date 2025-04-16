#### Description

Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py) using [this password](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt) to get [the flag](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en)?

Los scripts de Python se invocan de forma similar a los programas en la Terminal... ¿Puedes ejecutar [este script de Python](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py) usando [esta contraseña](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt) para obtener [la bandera](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en) ?

#### Consejos:
* Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py`
* $ man python

* Se descagaron los archivos que nos dieron con wget, se leyó pw.txt con cat `ac9bd0ffac9bd0ffac9bd0ffac9bd0ff`  porque venía la contraseña ahí. Se corrio el programa con : ` python3 ende.py -d flag.txt.en `

```
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wrangling$ wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py
--2025-04-15 12:15:05--  https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142, 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1328 (1.3K) [application/octet-stream]
Saving to: ‘ende.py’

ende.py            100%[================>]   1.30K  --.-KB/s    in 0s

2025-04-15 12:15:07 (157 MB/s) - ‘ende.py’ saved [1328/1328]

yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wrangling$ wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt
--2025-04-15 12:17:34--  https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 33 [application/octet-stream]
Saving to: ‘pw.txt’

pw.txt             100%[================>]      33  --.-KB/s    in 0s

2025-04-15 12:17:36 (2.26 MB/s) - ‘pw.txt’ saved [33/33]

yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wrangling$ wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en
--2025-04-15 12:17:45--  https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142, 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 140 [application/octet-stream]
Saving to: ‘flag.txt.en’

flag.txt.en        100%[================>]     140  --.-KB/s    in 0s

2025-04-15 12:17:47 (24.8 MB/s) - ‘flag.txt.en’ saved [140/140]

yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wrangling$ python3 ende.py -h
Usage: ende.py (-e/-d) [file]
Examples:
  To decrypt a file named 'pole.txt', do: '$ python ende.py -d pole.txt'

yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wrangling$ ls
ende.py  flag.txt.en  pw.txt
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wrangling$ cat pw.txt
ac9bd0ffac9bd0ffac9bd0ffac9bd0ff
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wrangling$ python3 ende.py -d flag.txt.en
Please enter the password:ac9bd0ffac9bd0ffac9bd0ffac9bd0ff
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wranglingyoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/3-Python-Wr
angling$
```

![[Pasted image 20250415122437.png]]
![[Pasted image 20250415122507.png]]
## Solución:
```
picoCTF{4p0110_1n_7h3_h0us3_ac9bd0ff}
```