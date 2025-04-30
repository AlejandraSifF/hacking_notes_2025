#### Description

Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.


#### Consejos:
1. How did pictures from the moon landing get sent back to Earth?
2. What is the CMU mascot?, that might help select a RX option
## Solución
```
picoCTF{beep_boop_im_in_space}
```
https://github.com/colaclanth/sstv


sstv -d message.wav -o flag.png
open flag.png 
