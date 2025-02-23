* Permisos
#### Description

Can you read files in the root file?

Additional details will be available after launching your challenge instance.

¿Puedes leer archivos en el archivo raíz?

Habrá detalles adicionales disponibles después de lanzar su instancia de desafío

The system admin has provisioned an account for you on the main server:`ssh -p 55479 picoplayer@saturn.picoctf.net`Password: `e3pn6lmvHt`

## Solución   

ssh -p 55479 picoplayer@saturn.picoctf.net
Contraseña:  `e3pn6lmvHt`
Después me fuí a root con sudo vi / root y cheque los varios archivos que había estaba la bandera en: .flag.txt

```
picoCTF{uS1ng_v1m_3dit0r_f6ad392b}
```
