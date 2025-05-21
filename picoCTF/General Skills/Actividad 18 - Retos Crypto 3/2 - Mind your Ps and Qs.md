#### Description

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)


#### Consejos:
1.  Bits are expensive, I used only a little bit over 100 to save money

#### Solución:
```
picoCTF{sma11_N_n0_g0od_73918962}
```

#### Terminal:
```
yoli@Yoli:~/Fundamentos_Seguridad/Actividad_18-Retos_Crypto_3/2Mind_your_Ps_and_Qs$ wget https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values
--2025-05-21 12:35:59--  https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142, 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 206 [application/octet-stream]
Saving to: ‘values’

values                    100%[===================================>]     206  --.-KB/s    in 0s

2025-05-21 12:35:59 (21.0 MB/s) - ‘values’ saved [206/206]

yoli@Yoli:~/Fundamentos_Seguridad/Actividad_18-Retos_Crypto_3/2Mind_your_Ps_and_Qs$ cat values
Decrypt my super sick RSA:
c: 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n: 1584586296183412107468474423529992275940096154074798537916936609523894209759157543

```

```
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
>>> e = 65537
>>> p = 2434792384523484381583634042478415057961
>>> q = 650809615742055581459820253356987396346063
>>> n = p * q
>>> n
1584586296183412107468474423529992275940096154074798537916936609523894209759157543
>>> tn = (p-1)*(q-1)
>>> d = inverse(e,tn)
>>> m = pow(c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639684640304028661985917
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_73918962}'
>>>
```
![[Pasted image 20250521143038.png]]


* EJ:

RsaCtfTool -n 1280678415822214057864524798453297819181910621573945477544758171055968245116423923 -e 65537 --decrypt 62324783949134119159408816513334912534343517300880137691662780895409992760262021 --attack factordb
