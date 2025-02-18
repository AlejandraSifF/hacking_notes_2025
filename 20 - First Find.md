Primer hallazgo

Unzip this archive and find the file named 'uber-secret.txt'
Download zip file.
Descomprima este archivo y busque el archivo llamado 'uber-secret.txt'
Descargar archivo zip
* **==Borrar archivos: Siloy-picoctf@webshell:~$ rm -rf** *==
* file . -name
## Solución 
```
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/501/files.zip
--2025-02-17 18:09:04--  https://artifacts.picoctf.net/c/501/files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3995553 (3.8M) [application/octet-stream]
Saving to: 'files.zip.1'

files.zip.1                  100%[=============================================>]   3.81M  1.82MB/s    in 2.1s    

2025-02-17 18:09:06 (1.82 MB/s) - 'files.zip.1' saved [3995553/3995553]

Siloy-picoctf@webshell:~$ unzip files.zip
Archive:  files.zip
replace files/satisfactory_books/more_books/37121.txt.utf-8? [y]es, [n]o, [A]ll, [N]one, [r]ename: A
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
Siloy-picoctf@webshell:~$ cd adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
-bash: cd: adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/: No such file or directory
Siloy-picoctf@webshell:~$ cd adequate_books/more_books/.secret/deeper_secrets/deepest_secrets 
-bash: cd: adequate_books/more_books/.secret/deeper_secrets/deepest_secrets: No such file or directory
Siloy-picoctf@webshell:~$ ls
Addadshashanammu      big-zip-files        big-zip-files.zip.2  files        flag        salida    strings  warm.2
Addadshashanammu.zip  big-zip-files.zip    enc_flag             files.zip    grep.php    static    warm     warm.3
README.txt            big-zip-files.zip.1  file                 files.zip.1  grep.php.1  static.1  warm.1
Siloy-picoctf@webshell:~$ cd files.zip
-bash: cd: files.zip: Not a directory
Siloy-picoctf@webshell:~$ cd files    
Siloy-picoctf@webshell:~/files$ ls
13771.txt.utf-8  14789.txt.utf-8  acceptable_books  adequate_books  satisfactory_books
Siloy-picoctf@webshell:~/files$ cd adequate_books/
Siloy-picoctf@webshell:~/files/adequate_books$ ls
44578.txt.utf-8  46804-0.txt  more_books
Siloy-picoctf@webshell:~/files/adequate_books$ cd more_books 
Siloy-picoctf@webshell:~/files/adequate_books/more_books$ ls
1023.txt.utf-8
Siloy-picoctf@webshell:~/files/adequate_books/more_books$ cd .secret
Siloy-picoctf@webshell:~/files/adequate_books/more_books/.secret$ ls
deeper_secrets
Siloy-picoctf@webshell:~/files/adequate_books/more_books/.secret$ cd deeper_secrets/
Siloy-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets$ ls
deepest_secrets
Siloy-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets$ cd deepest_secrets/
Siloy-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ ls
uber-secret.txt
Siloy-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ cat uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}

```
