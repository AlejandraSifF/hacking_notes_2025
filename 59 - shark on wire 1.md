#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

![[Pasted image 20250407123205.png]]
#### Archivos pcap:
Un **archivo PCAP** (Packet Capture) es un tipo de archivo que contiene un **registro de paquetes de red capturados**. Es decir, guarda toda la información que viaja por una red (como Ethernet, Wi-Fi, etc.) durante una sesión de captura, incluyendo encabezados y contenido de los paquetes.

---

### 📦 ¿Qué contiene un archivo `.pcap`?

- Direcciones IP de origen y destino.
    
- Protocolos utilizados (TCP, UDP, ICMP, HTTP, DNS, etc.).
    
- Contenido (payload) de los paquetes.
    
- Tiempos de llegada de cada paquete.
    
- Puertos de comunicación, flags, tamaño, entre otros detalles técnicos.
    

---

### 🛠️ ¿Para qué sirve?

- **Análisis de red** (diagnóstico de problemas de conectividad, rendimiento).
    
- **Seguridad informática** (detección de intrusiones, análisis forense).
    
- **Ingeniería inversa** de tráfico o protocolos.
    
- **Estudio académico** de redes.
    

---

### 🔍 ¿Cómo se abre?

Para ver el contenido de un `.pcap`, se necesita una herramienta especializada como:

- **Wireshark** (gratuita y muy popular):  
    Interfaz gráfica para visualizar, filtrar y analizar el tráfico capturado.
    
- **tcpdump** (línea de comandos en Linux/Mac):  
    Para capturar y leer `.pcap` directamente desde la terminal.
    
- **Tshark**:  
    Versión de línea de comandos de Wireshark.
    

---

### Ejemplo de uso:

bash

Copiar código

`tcpdump -i eth0 -w captura.pcap`

> Captura paquetes de la interfaz `eth0` y los guarda en el archivo `captura.pcap`.
> 

## Paso a paso:

![[Pasted image 20250407123931.png]]

![[Pasted image 20250407124109.png]]
![[Pasted image 20250407124131.png]]
![[Pasted image 20250407124202.png]]



* esta en el 6:

![[Pasted image 20250407124256.png]]

## Solución 
```
picoCTF{StaT31355_636f6e6e}
```