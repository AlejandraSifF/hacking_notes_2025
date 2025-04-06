https://regexr.com/
#### Description

How about trying to match a regular expression

Additional details will be available after launching your challenge instance.


Las **expresiones regulares (regex)** son patrones utilizados para buscar y manipular cadenas de texto. Son muy útiles en tareas como validación de datos, extracción de información y búsqueda avanzada en archivos o bases de datos.

## 📌 **Ejemplos de uso de expresiones regulares:**

### 1️⃣ **Validar correos electrónicos**

regex

Copiar código

`^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$`

🔹 **Ejemplo válido:** `usuario123@gmail.com`  
🔹 **Ejemplo no válido:** `usuario@@gmail..com`

---

### 2️⃣ **Validar números de teléfono (Formato internacional)**

regex

Copiar código

`^\+?[0-9]{1,3}[-.\s]?[0-9]{3,4}[-.\s]?[0-9]{3,4}$`

🔹 **Ejemplo válido:** `+52 123-456-7890`  
🔹 **Ejemplo no válido:** `123-abc-789`

---

### 3️⃣ **Extraer direcciones IP**

regex

Copiar código

`\b(?:[0-9]{1,3}\.){3}[0-9]{1,3}\b`

🔹 **Ejemplo válido:** `192.168.1.1`  
🔹 **Ejemplo no válido:** `999.999.999.999` (Fuera de rango)

---

### 4️⃣ **Buscar fechas en formato DD/MM/AAAA**

regex

Copiar código

`\b(0[1-9]|[12][0-9]|3[01])/(0[1-9]|1[0-2])/\d{4}\b`

🔹 **Ejemplo válido:** `25/12/2023`  
🔹 **Ejemplo no válido:** `32/13/2023`

---

### 5️⃣ **Encontrar palabras específicas en un texto**

Si quieres buscar palabras como `error`, `warning` o `fail` en un archivo de logs:

regex

Copiar código

`\b(error|warning|fail)\b`

🔹 **Ejemplo válido:** `System error detected`  
🔹 **Ejemplo no válido:** `errored` (porque no es exactamente `error`)

---

### 6️⃣ **Detectar URLs en un texto**

regex

Copiar código

`https?://[^\s]+`

🔹 **Ejemplo válido:** `https://openai.com`  
🔹 **Ejemplo no válido:** `www.openai.com` (falta `http://` o `https://`)

---

## 📌 **¿Dónde se usan las expresiones regulares?**

✅ **Lenguajes de programación:** Python, JavaScript, C, Java, VHDL (en algunos casos).  
✅ **Sistemas operativos:** Comandos `grep`, `sed`, `awk` en Linux.  
✅ **Bases de datos:** PostgreSQL, MySQL, MongoDB.  
✅ **Procesamiento de texto:** Filtrado de logs, validación de formularios, reemplazo de patrones.

## Ejemplo:
Construye una expresión regular que valide los sig elementos: 
333-333-3333
333.333.3333
```
^\d{3}[-.]\d{3}[-.]\d{4}$


```

Código fuente

picoCTF{^p.....F!?}

![[Pasted image 20250402121542.png]]


![[Pasted image 20250402121519.png]]
## Solución
```
picoCTF{succ3ssfully_matchtheregex_0694f25b}
```