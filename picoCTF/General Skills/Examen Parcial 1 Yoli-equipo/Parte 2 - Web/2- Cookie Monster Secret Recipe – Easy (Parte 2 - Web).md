#### Description

Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:49480/) and good luck.

El Monstruo Comegalletas ha escondido su receta secreta de galletas en su sitio web. Como aspirante a detective de galletas, tu misión es descubrir este delicioso secreto. ¿Podrás ser más astuto que el Monstruo Comegalletas y encontrar la receta oculta?Puedes acceder al Monstruo de las Galletas [aquí](http://verbal-sleep.picoctf.net:49480/) y buena suerte.

* **Consejos:**
	* Sometimes, the most important information is hidden in plain sight. Have you checked all parts of the webpage?
	  A veces, la información más importante está oculta a simple vista. ¿Has revisado toda la página web?
	  
	* Cookies aren't just for eating - they're also used in web technologies!
	  Las cookies no sólo se utilizan para comer: ¡también se utilizan en las tecnologías web!
	  
	* Web browsers often have tools that can help you inspect various aspects of a webpage, including things you can't see directly.
	  Los navegadores web a menudo tienen herramientas que pueden ayudarle a inspeccionar varios aspectos de una página web, incluidas cosas que no puede ver directamente.

![[Pasted image 20250414195627.png]]
* Inspeccionar y en aplicacion, se copia el valor de la cookie:
![[Pasted image 20250414195831.png]]

* En Burp Suite se copia cookie en decoder y en desde base 64:
![[Pasted image 20250414200008.png]]
* o en Cyberchef:
![[Pasted image 20250414200056.png]]

## Solución:
```
picoCTF{c00k1e_m0nster_l0ves_c00kies_AC8FCD75}
```

## Referencias:
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnRqTURCck1XVmZiVEJ1YzNSbGNsOXNNSFpsYzE5ak1EQnJhV1Z6WDBGRE9FWkRSRGMxZlElM0QlM0Q&oeol=CR
