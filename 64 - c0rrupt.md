#### Description

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

#### Consejos:
1. Try fixing the file header

## Solución
```
picoCTF{c0rrupt10n_1847995}

```

 wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
--2025-04-28 12:40:00--  https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery

pHYs es de png -> imagen 
![[Pasted image 20250428124436.png]]
### ¿Qué son los **magic bytes**?

Los **magic bytes** (o **magic numbers**) son **los primeros bytes** de un archivo que **identifican su tipo**.

> Es como una **huella digital** al inicio del archivo para que los programas sepan **qué tipo de archivo** es (imagen, video, audio, ejecutable, etc.), **sin necesidad de ver la extensión `.jpg`, `.png`, `.wav`, etc.**

---

### Ejemplos de magic bytes comunes:

|Tipo de archivo|Magic Bytes (en hexadecimal)|Significado|
|---|---|---|
|PNG|`89 50 4E 47`|Empieza con "‰PNG"|
|JPG|`FF D8 FF`|Indica imagen JPEG|
|GIF|`47 49 46 38`|Indica imagen GIF|
|PDF|`25 50 44 46`|"%PDF"|
|ZIP|`50 4B 03 04`|Archivo comprimido|
|WAV (audio)|`52 49 46 46` (`RIFF`)|Archivo RIFF/WAV|

---

### ¿Por qué son importantes?

- Los sistemas operativos o programas pueden **detectar** el tipo de archivo **aunque la extensión esté mal o falte**.
    
- Se usan en **análisis forense** y **ciberseguridad** para descubrir archivos ocultos, modificados o disfrazados.
    
- Algunos retos de **CTF** (como parece ser tu caso 👀) ocultan información en archivos revisando o alterando sus **magic bytes**.
    

---

### ¿Cómo ver los magic bytes?

Puedes usar en la terminal:

bash

Copiar código

`xxd archivo.ext | head`

o

bash

Copiar código

`hexdump -C archivo.ext | head`

Y verás el contenido en hexadecimal, donde los **primeros bytes** son los "magic bytes".

---

**Ejemplo real:**

Archivo PNG (`prueba.png`):

bash

Copiar código

`xxd prueba.png | head`

Sale algo así:

yaml

Copiar código

`00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG......IHDR`

===================

sudo apt install pngcheck


8950 4e47 0d0a 1a0a: al inicio para reparar el encabezado:
![[Pasted image 20250428124937.png]]
y sale ya PNG:
![[Pasted image 20250428125036.png]]

IH:
![[Pasted image 20250428125618.png]]


![[Pasted image 20250428125753.png]]
![[Pasted image 20250428125859.png]]


Faltó algo:
