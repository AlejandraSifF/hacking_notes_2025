#### Description

Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/56816/` ([link](https://jupiter.challenges.picoctf.org/problem/56816/)) or http://jupiter.challenges.picoctf.org:56816


Ofuscación.

![[Pasted image 20250324132003.png]]
## Solución

```
allow pasting

var _0x5a46 = ["37115}", "_again_3", "this", "Password Verified", "Incorrect password", "getElementById", "value", "substring", "picoCTF{", "not_this"];

undefined

var f = ["37115}", "_again_3", "this", "Password Verified", "Incorrect password", "getElementById", "value", "substring", "picoCTF{", "not_this"];

undefined

f[8] + f[9]

'picoCTF{not_this'

f[8] + f[9] + f [1] + f[0]

'picoCTF{not_this_again_337115}'

picoCTF{not_this_again_337115}
```
