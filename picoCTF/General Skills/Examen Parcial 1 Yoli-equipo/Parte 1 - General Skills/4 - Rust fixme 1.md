#### Description

Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
¿Has oído hablar de Rust? ¡Corrige los errores de sintaxis en este archivo de Rust para imprimir la bandera!Descargue el código de Rust [aquí](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz) .

#### Consejos:
1.  Cargo is Rust's package manager and will make your life easier. See the getting started page [here](https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)
2. [println!](https://doc.rust-lang.org/std/macro.println.html)
3. Rust has some pretty great compiler error messages. Read them maybe?

* Se descarga el archivo:
  `wget https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz`
  ![[Pasted image 20250415123610.png]]
* Poner: `tar xvzf fixme1.tar.gz`
  ![[Pasted image 20250415123708.png]]
* Irnos a fixme1 y compilar con `cargo build `
  Nos dirá que tenemos 3 errores por lo que se tendrá que corregir:
  ![[Pasted image 20250415123834.png]]
* Nos vamos a src y corregimos el código  `nano mian.rs`
  ![[Pasted image 20250415124005.png]]
* Correcciones:
  ![[Pasted image 20250415124109.png]]
* Se vuelve a compliar y correr el programa y ya nos da la bandera:
  ![[Pasted image 20250415124227.png]]
## Solución:
```
picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}
```