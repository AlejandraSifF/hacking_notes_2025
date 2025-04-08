#### Description

There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

![[Pasted image 20250407130201.png]]


![[Pasted image 20250407130118.png]]

* Otra forma:
gem install zsteg
zsteg buildings.png:
![[Pasted image 20250407131144.png]]

zsteg -E 'bl.rgb.lsb' buildings.png

```
picoCTF{h1d1ng_1n_th3_b1t5}
```

## Referencias:
https://stylesuxx.github.io/steganography/
