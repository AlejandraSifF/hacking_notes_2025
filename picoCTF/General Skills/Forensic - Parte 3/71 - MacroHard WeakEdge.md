#### Description

I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/2e739f9e0dc9f4c1556ea6b033c3ec8e/Forensics%20is%20fun.pptm)

## Solución 
```
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```

Archivo pptm:
Un archivo **`.pptm`** es una **presentación de Microsoft PowerPoint** que **contiene macros**. La extensión `.pptm` indica que:

- Es compatible con **PowerPoint 2007 o versiones posteriores**.
    
- Está basado en el **formato Office Open XML**.
    
- Puede incluir **macros escritas en VBA (Visual Basic for Applications)** para automatizar tareas, como botones interactivos, cálculos o animaciones personalizadas.


#### Pasos:
descomprimimos el documento
hidden es oculto... da una pista:
Nos vamos a esa carpeta y leemos hidden, eliminamos espacios y base 64 
![[Pasted image 20250505132145.png]]
![[Pasted image 20250505132215.png]]
