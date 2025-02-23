Description
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?
You can download the challenge files here:
challenge.zip

¡Mi equipo ha estado trabajando muy duro en nuevas funciones para nuestro programa de impresión de banderas! Me pregunto cómo trabajarán juntas.
Puedes descargar los archivos del desafío aquí:
desafío.zip

Hits:
* git branch -aTe permitirá ver las sucursales disponibles
* ¿Cómo se puede llevar el archivo 'diffs' a la rama principal? ¡No olvides hacerlo `git config`!
* Los conflictos de fusión pueden ser complicados. Prueba con un editor de texto como nano, emacs o vim.
## Solución:


```

Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/178/challenge.zip
--2025-02-23 05:14:50--  https://artifacts.picoctf.net/c_titan/178/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.71, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24640 (24K) [application/octet-stream]
Saving to: 'challenge.zip.3'

challenge.zip.3              100%[=============================================>]  24.06K  --.-KB/s    in 0.002s  

2025-02-23 05:14:50 (12.2 MB/s) - 'challenge.zip.3' saved [24640/24640]

Siloy-picoctf@webshell:~$ unzip challenge.zip.3
Archive:  challenge.zip.3
replace drop-in/.git/description? [y]es, [n]o, [A]ll, [N]one, [r]ename: y
  inflating: drop-in/.git/description  
replace drop-in/.git/hooks/applypatch-msg.sample? [y]es, [n]o, [A]ll, [N]one, [r]ename: A
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
  inflating: drop-in/.git/info/exclude  
 extracting: drop-in/.git/refs/heads/main  
   creating: drop-in/.git/refs/heads/feature/
 extracting: drop-in/.git/refs/heads/feature/part-1  
 extracting: drop-in/.git/refs/heads/feature/part-2  
 extracting: drop-in/.git/refs/heads/feature/part-3  
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
 extracting: drop-in/.git/objects/77/d6ceca6fe23b57d88cf16f20003e10d6715690  
 extracting: drop-in/.git/objects/b9/32e8c048154a46d224cd7691c99dc8cb88164a  
 extracting: drop-in/.git/objects/22/58a0f267d57e8b6025e2a020b77fac7a553c92  
 extracting: drop-in/.git/objects/6e/17fb3a35364b4f9bb8bef8b5e6a5af2d3e7dfa  
 extracting: drop-in/.git/objects/43/e44dd37ba0c0adc3d78d0b85d699859ec8d75c  
 extracting: drop-in/.git/objects/8e/ea0627726fc363246015cb4c7e927e70286e87  
 extracting: drop-in/.git/objects/7a/b4e25c0cd108374b2275fdb1fcdf635e591833  
 extracting: drop-in/.git/objects/d1/f3407cee4479c075997b497fa290ca636fe258  
   creating: drop-in/.git/objects/05/
 extracting: drop-in/.git/objects/05/db9e274ff691e0f9fb492403b570629eb80aa9  
 extracting: drop-in/.git/objects/4f/136da027f9a97032d53dd5f667dd6c7852737c  
 extracting: drop-in/.git/objects/dd/f6fd2129098bf677ac010259a2a642060aea47  
   creating: drop-in/.git/objects/65/
 extracting: drop-in/.git/objects/65/5c7bfebe9c221369ab00ac7374d0d4bd4d62a9  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
  inflating: drop-in/.git/logs/HEAD  
  inflating: drop-in/.git/logs/refs/heads/main  
   creating: drop-in/.git/logs/refs/heads/feature/
  inflating: drop-in/.git/logs/refs/heads/feature/part-1  
  inflating: drop-in/.git/logs/refs/heads/feature/part-2  
  inflating: drop-in/.git/logs/refs/heads/feature/part-3  
  inflating: drop-in/flag.py         
Siloy-picoctf@webshell:~$ git init
Reinitialized existing Git repository in /home/Siloy-picoctf/.git/
Siloy-picoctf@webshell:~$ flag.py
-bash: flag.py: command not found
Siloy-picoctf@webshell:~$ cd drop-in
Siloy-picoctf@webshell:~/drop-in$ flag.py
-bash: flag.py: command not found
Siloy-picoctf@webshell:~/drop-in$ git branch -a

[7]+  Stopped                 git branch -a
Siloy-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
Siloy-picoctf@webshell:~/drop-in$ git log 
[8]+  Stopped                 git log
Siloy-picoctf@webshell:~/drop-in$ git log feature/part-2

[9]+  Stopped                 git log feature/part-2
Siloy-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Already on 'feature/part-1'
Siloy-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')Siloy-picoctf@webshell:~/drop-in$ git log feature/part-2

[10]+  Stopped                 git log feature/part-2
Siloy-picoctf@webshell:~/drop-in$ git diff 05db9e274ff691e0f9fb492403b570629eb80aa9 -- flag.py
        

Siloy-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Already on 'feature/part-1'
Siloy-picoctf@webshell:~/drop-in$ git log feature/part-1

[12]+  Stopped                 git log feature/part-1
Siloy-picoctf@webshell:~/drop-in$ git diff 8eea0627726fc363246015cb4c7e927e70286e87 -- flag.py

[13]+  Stopped                 git diff 8eea0627726fc363246015cb4c7e927e70286e87 -- flag.py
Siloy-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')Siloy-picoctf@webshell:~/drop-in$ git diff 8eea0627726fc363246015cb4c7e927e70286egit log feature/part-2
Siloy-picoctf@webshell:~/drop-in$ git diff 05db9e274ff691e0f9fb492403b570629eb80aa9 -- flag.py
[15]+  Stopped                 git diff 05db9e274ff691e0f9fb492403b570629eb80aa9 -- flag.py
Siloy-picoctf@webshell:~/drop-in$ git log feature/part-3

[16]+  Stopped                 git log feature/part-3
Siloy-picoctf@webshell:~/drop-in$ git diff 655c7bfebe9c221369ab00ac7374d0d4bd4d62a9 -- flag.py

[17]+  Stopped                 git diff 655c7bfebe9c221369ab00ac7374d0d4bd4d62a9 -- flag.py
Siloy-picoctf@webshell:~/drop-in$ 

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_6c06cec1}
```
