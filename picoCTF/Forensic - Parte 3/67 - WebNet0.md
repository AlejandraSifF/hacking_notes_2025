#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

####  Consejos:
1.  Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?
## Solución 
```
picoCTF{nongshim.shrimp.crackers}
```

#### Usando wireshark 
TLS y selecciona archivo de llave 
![[Pasted image 20250505122232.png]]
![[Pasted image 20250505122253.png]]
#### Otra forma en terminal:

ssldump -r capture.pcap -k picopico.key -d | grep pico -A 2
![[Pasted image 20250505122511.png]]
