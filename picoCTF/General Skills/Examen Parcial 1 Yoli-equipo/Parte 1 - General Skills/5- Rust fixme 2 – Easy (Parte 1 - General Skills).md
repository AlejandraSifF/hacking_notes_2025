#### Description

The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).

* **Instalar Rustc**: https://forge.rust-lang.org/infra/release-archives.html
  * **Dar permisos:**
    * *chmod +x rustup-init.sh*
    * *./rustup-init.sh*
  * **Después se cierra terminal y se abre una nueva:**
	  * *source $HOME/.cargo/env*
	  * *rustc --version*
	  * *cargo --version*

* **Descargar zip:** wget https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz

* **Descomprimir:**
	* tar -xvzf fixme2.tar.gz
    * ls

* Ir a **fixme2**:
    * *cd fixme2*

* **Ejecutar con:**
    * *cargo build*


* **Después:**

*nano main.rs*
![[Pasted image 20250414192330.png]]
después: "mut"
![[Pasted image 20250414192501.png]]
![[Pasted image 20250414192622.png]]
![[Pasted image 20250414192743.png]]
*cd src*

**Respuesta:**
![[Pasted image 20250414192957.png]]
## Solución 
```
 picoCTF{4r3_y0u_h4v1n5_fun_y31?}
```


## Referencias:
https://forge.rust-lang.org/infra/release-archives.html