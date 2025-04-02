#### Description

There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
Hay un sitio web en funcionamiento en `https://jupiter.challenges.picoctf.org/problem/50009/`( [enlace](https://jupiter.challenges.picoctf.org/problem/50009/) ) o http://jupiter.challenges.picoctf.org:50009. ¿Crees que puedes iniciar sesión? ¡Intenta ver si puedes!
## Pistas:
* There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database? 
  No parece haber muchas maneras de interactuar con esto. Me pregunto si los usuarios se guardan en una base de datos.
  
* Try to think about how the website verifies your login.
  Intente pensar en cómo el sitio web verifica su inicio de sesión.


## *Inyección SQL* :  
La **inyección SQL (SQL Injection)** es una vulnerabilidad de seguridad que ocurre cuando un atacante inserta o "inyecta" código SQL malicioso en una consulta que una aplicación ejecuta en una base de datos. Esto puede permitir que el atacante acceda, modifique o incluso elimine datos sin autorización.

// Entrada del usuario sin sanitizar
$usuario = $_GET['usuario'];
$password = $_GET['password'];

// Consulta vulnerable
$query = "SELECT * FROM usuarios WHERE nombre = '$usuario' AND password = '$password'";
$result = mysqli_query($conn, $query);


## Solución
```
picoCTF{s0m3_SQL_fb3fe2ad}
```

Era así en el código fuente:

![[Pasted image 20250331130823.png]]