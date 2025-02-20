#### Description

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
Ejecute el `runme.py`script para obtener la bandera. Descargue el script con su navegador o con `wget`el shell web.[Descargar el script Python runme.py](https://artifacts.picoctf.net/c/34/runme.py)

Hints:
1. If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.                Si tienes Python en tu computadora, puedes descargar el script normalmente y ejecutarlo. De lo contrario, usa el `wget`comando en el shell web.

2. To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'. Para utilizarlo `wget`en el webshell, primero haga clic derecho en el enlace de descarga y seleccione 'Copiar enlace' o 'Copiar dirección de enlace'

3. Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it! Escribe todo lo que aparece después del signo de dólar en el webshell: `$ wget` , luego pega el enlace después del espacio `wget`y presiona Enter. ¡Esto descargará el script en el webshell para que puedas ejecutarlo!

4. Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 runme.py` You should have the flag now! Finalmente, para ejecutar el script, escribe todo lo que está después del signo de dólar y luego presiona Enter: ¡ `$ python3 runme.py`Ahora deberías tener la bandera!

## Solución 
```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2025-02-20 03:55:46--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                     100%[=============================================>]     270  --.-KB/s    in 0s      

2025-02-20 03:55:46 (273 MB/s) - 'runme.py' saved [270/270]

Siloy-picoctf@webshell:~$ python3 runme.py
```
