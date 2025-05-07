
#### Description

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz)
#### Consejos:
1. 

## Solución:
```
picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}
```

gzip -d dds1-alpine.flag.img
ls -lah dds1-alpine.flag.img
![[Pasted image 20250507124125.png]]

### 🔍 ¿Qué puede ser `extion.img`?

1. **¿Un archivo de imagen de disco?**  
    Si es un archivo `.img` (como los de sistemas de archivos tipo Linux), podrías estar intentando **analizar una imagen forense** de un disco o partición. En ese caso, podrías usar herramientas como:
    
    - `binwalk extion.img`
        
    - `foremost -i extion.img`
        
    - `mount` (para montar la imagen si contiene un sistema de archivos reconocible)
        
    - `fdisk -l extion.img` o `mmls extion.img` (para ver particiones)

![[Pasted image 20250507124401.png]]
![[Pasted image 20250507124540.png]]
