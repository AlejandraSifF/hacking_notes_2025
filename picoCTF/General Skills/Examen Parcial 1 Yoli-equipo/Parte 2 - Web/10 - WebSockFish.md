#### Description

Can you win in a convincing manner against this chess bot? He won't go easy on you!You can find the challenge [here](http://verbal-sleep.picoctf.net:57518/).

#### Consejos:
1. Try understanding the code and how the websocket client is interacting with the server

Nos vamos a inspeccionar y a consola:
![[Pasted image 20250415192417.png]]
ponemos:
* `sendMessage("mate -10")`
* `sendMessage("eval -1000000")`
  ![[Pasted image 20250415192516.png]]


## Solución:
```
picoCTF{c1i3nt_s1d3_w3b_s0ck3t5_c0789e29}
```