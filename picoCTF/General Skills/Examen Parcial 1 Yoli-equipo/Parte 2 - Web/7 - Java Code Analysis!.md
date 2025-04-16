#### Description

BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!

Additional details will be available after launching your challenge instance.
BookShelf Pico, mi servicio premium de lectura de libros en línea. Creo que mi sitio web es súper seguro. ¡Te reto a que me demuestres lo contrario leyendo el libro "Flag"! Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

#### Consejos:
1.  Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2. The 'role' and 'userId' fields in the JWT can be of interest to you!
3. The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
4. Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.

* Entramos con user user  
* Inspeccionamos la página y nos vamos a Application copiamos `eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiRnJlZSIsImlzcyI6ImJvb2tzaGVsZiIsImV4cCI6MTc0NTM2ODA4MCwiaWF0IjoxNzQ0NzYzMjgwLCJ1c2VySWQiOjEsImVtYWlsIjoidXNlciJ9.M2wqINNIgyjj9R3Zerd0E8RtBPekDFepu2zLtt476JA`
  ![[Pasted image 20250415185135.png]]
* Y lo pegamos en https://jwt.io/
  Cambiamos esto:
  ![[Pasted image 20250415185159.png]]
* Ahora esto:
  `eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NDUzNjkwNjcsImlhdCI6MTc0NDc2NDI2NywidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.fpTU7lXRzgls6QOKVCw2c_huINPnjG3eP21CpfjuFaY`
  lo pegamos:
  ![[Pasted image 20250415185238.png]]
* Reiniciamos la página y nos da la llave:
  ![[Pasted image 20250415185301.png]]

## Solución:
```
picoCTF{w34k_jwt_n0t_g00d_42f5774a}
```