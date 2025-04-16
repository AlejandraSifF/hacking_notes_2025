#### Description

Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.

Additional details will be available after launching your challenge instance.

#### Consejos:
1.  Explore backend development with us.
2. The head was dumped.


* Checamos el link : http://verbal-sleep.picoctf.net:49620/ y lo inspeccionamos, y encontrsmos `api`-docs :
  ![[Pasted image 20250415150424.png]]
* Esto nos lleva a: http://verbal-sleep.picoctf.net:49620/api-docs/#/, nos vamos a este y nos dará un archivo para descargar:
  ![[Pasted image 20250415150530.png]]
  
* Lo leemos en la terminal de Linux con: ` cat heapdump-1744750618894.heapsnapshot | grep "picoCTF"` y nos sale todo lo que tiene picoCTF:
  ![[Pasted image 20250415150701.png]]
  Nos da al inicio la bandera.
  
## Solución
```
picoCTF{Pat!3nt_15_Th3_K3y_46022a05}
```