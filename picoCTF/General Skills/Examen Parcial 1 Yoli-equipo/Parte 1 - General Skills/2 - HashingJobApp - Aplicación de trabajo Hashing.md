#### Description

If you want to hash with the best, beat this test!

Additional details will be available after launching your challenge instance.

¡Si quieres competir con los mejores, supera este test!

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

`nc saturn.picoctf.net 61882`

#### Consejos:
* You can use a commandline tool or web app to hash text.
  Puede utilizar una herramienta de línea de comandos o una aplicación web para convertir texto en hash
  
* Press Ctrl and c on your keyboard to close your connection and return to the command prompt.
  Presione Ctrl y c en su teclado para cerrar su conexión y regresar al símbolo del sistema.

Copiamos `nc saturn.picoctf.net 61882` en la terminal y nos dice que se tiene que convertir el texto que esta entre las comillas simples a md5, con esto nos da la bandera. Nos apoyamos usando cyberchef.
```
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte1-General-Skills/2-HashingJobApp$ nc saturn.picoctf.net 61882
Please md5 hash the text between quotes, excluding the quotes: 'commuting'
Answer:
d2c3874ec246fb1858841223ffe4992e
d2c3874ec246fb1858841223ffe4992e
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Adam Sandler'
Answer:
39b415aa8ea163d51597193cd21b52b9
39b415aa8ea163d51597193cd21b52b9
Incorrect. Try again?
Answer:
dfaa815a18f38cd5737f9fd73b907d6e
dfaa815a18f38cd5737f9fd73b907d6e
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Adolf Hitler'
Answer:
540dea05a35b0fc9a050f36db954a484
540dea05a35b0fc9a050f36db954a484
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}
```
![[Pasted image 20250415120851.png]]
## Solución:
```
picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}
```


## Referencias 
https://gchq.github.io/CyberChef/#recipe=MD5()&input=QWRvbGYgSGl0bGVy
