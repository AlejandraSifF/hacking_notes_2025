What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.
## Solución 1
Cyberchef
```
Input: bDNhcm5fdGgzX3IwcDM1

Output: l3arn_th3_r0p35
picoCTF{l3arn_th3_r0p35}
```

## Solución 2
```
Siloy-picoctf@webshell:~$ echo bDNhcm5fdGgzX3IwcDM1 | base64 -d
l3arn_th3_r0p35 
Siloy-picoctf@webshell:~$ 

picoCTF{l3arn_th3_r0p35}
```

## Solución 
Usando python
```
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1')
b'l3arn_th3_r0p35'

picoCTF{l3arn_th3_r0p35}
```
## Referencias
...
