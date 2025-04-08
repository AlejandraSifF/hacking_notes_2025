#### Description

Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/00efdf2961da1e21470ffc0d496c3cc2/pico_img.png).
![[Pasted image 20250407122651.png]]


![[Pasted image 20250407122215.png]]

* Otra forma buscando los metadatos 
![[Pasted image 20250407122344.png]]
![[Pasted image 20250407122430.png]]

* Me faltó: sudo snap install gimp  

#### Metadatos

Los **metadatos** son datos que describen otros datos. Es decir, son información adicional que ayuda a entender, organizar o gestionar un recurso, archivo o conjunto de datos.

### Ejemplos para entenderlo mejor:

- En una **foto**:
    
    - Los metadatos pueden incluir: fecha en que se tomó, resolución, modelo de cámara, ubicación GPS, etc.
        
- En un **archivo de texto o documento**:
    
    - Autor, fecha de creación, fecha de última modificación, tamaño del archivo, etc.
        
- En una **canción MP3**:
    
    - Nombre del artista, álbum, año, género musical, duración, etc.
        
- En bases de datos:
    
    - Los metadatos describen las tablas, campos, tipos de datos, relaciones, restricciones, etc.

### ¿Para qué sirven?

- Facilitan la **búsqueda** y organización.
    
- Permiten una mejor **gestión** de la información.
    
- Ayudan a entender el **contenido sin tener que abrir** el archivo.
    
- Son clave en temas como **seguridad, privacidad y auditoría**.
### 📷 **Imágenes (JPG, PNG, etc.)**

- **Windows**: Haz clic derecho > Propiedades > Detalles.
    
- **Mac**: Clic derecho > Obtener información o usar la app Vista Previa.
    
- **Web**:
    
    - [ExifTool](https://exiftool.org/): Muy completo, para terminal.
        
    - [Get-Metadata.com](https://www.get-metadata.com/): Subes la imagen y te da los metadatos.
        
- **Aplicaciones**:
    
    - **Adobe Lightroom** / Photoshop: Muestran metadatos EXIF completos.
## Solución 
```
picoCTF{s0_m3ta_fec06741}
```