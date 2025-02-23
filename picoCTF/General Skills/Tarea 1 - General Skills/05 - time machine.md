#### Description

What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/67/challenge.zip)
  
¿En qué estaba trabajando por última vez? Recuerdo que escribí una nota para ayudarme a recordar...Puedes descargar los archivos del desafío aquí:

- [desafío.zip](https://artifacts.picoctf.net/c_titan/67/challenge.zip)

## Solución 
```
Siloy-picoctf@webshell:~$ rm -rf
Siloy-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/67/challenge.zip
--2025-02-23 04:55:24--  https://artifacts.picoctf.net/c_titan/67/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.42, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17743 (17K) [application/octet-stream]
Saving to: 'challenge.zip.1'

challenge.zip.1              100%[=============================================>]  17.33K  --.-KB/s    in 0.007s  

2025-02-23 04:55:24 (2.54 MB/s) - 'challenge.zip.1' saved [17743/17743]

Siloy-picoctf@webshell:~$ unzip challenge.zip.1
Archive:  challenge.zip.1
replace drop-in/message.txt? [y]es, [n]o, [A]ll, [N]one, [r]ename: yes
  inflating: drop-in/message.txt     
replace drop-in/.git/description? [y]es, [n]o, [A]ll, [N]one, [r]ename: A 
  inflating: drop-in/.git/description  
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
 extracting: drop-in/.git/refs/heads/master  
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
   creating: drop-in/.git/objects/25/
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
   creating: drop-in/.git/objects/b9/
 extracting: drop-in/.git/objects/b9/2bdd8ec87a21ba45e77bd9bed3e4893faafd0f  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
  inflating: drop-in/.git/logs/HEAD  
  inflating: drop-in/.git/logs/refs/heads/master  
Siloy-picoctf@webshell:~$ cd drop-in
Siloy-picoctf@webshell:~/drop-in$ git init
Reinitialized existing Git repository in /home/Siloy-picoctf/drop-in/.git/
Siloy-picoctf@webshell:~/drop-in$ git log

[1]+  Stopped                 git log
Siloy-picoctf@webshell:~/drop-in$ ^C



picoCTF{t1m3m@ch1n3_5cde9075}
```