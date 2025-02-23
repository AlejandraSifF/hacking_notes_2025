mm
Description
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.
Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!
You can download the challenge files here:
challenge.zip
Additional details will be available after launching your challenge instance.

¿Quieres jugar a un juego? A medida que uses más el shell, ¡quizás te interese saber cómo funcionan! La búsqueda binaria es un algoritmo clásico que se utiliza para encontrar rápidamente un elemento en una lista ordenada. ¿Puedes encontrar la bandera? Tendrás 1000 posibilidades y solo 10 intentos.
La ciberseguridad suele implicar una enorme cantidad de datos que analizar: registros, informes de vulnerabilidades y análisis forense. Practicar los conceptos básicos de forma manual puede resultarte útil en el futuro cuando tengas que crear tus propias herramientas.
Puedes descargar los archivos del desafío aquí:
desafío.zip
Habrá detalles adicionales disponibles después de lanzar su instancia de desafío.

ssh -p 56189 ctf-player@atlas.picoctf.net
Using the password 83dcefb7. Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden!

## Solución 
```
Siloy-picoctf@webshell:~/drop-in$ ssh -p 56189 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:56189 ([18.217.83.136]:56189)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:56189' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: yes
Please enter a valid number.
Enter your guess: 1
Higher! Try again.
Enter your guess: 2
Higher! Try again.
Enter your guess: 1000
Lower! Try again.
Enter your guess: ^CExiting is not allowed.
 
Please enter a valid number.
Enter your guess: ls
Please enter a valid number.
Enter your guess: 41
Higher! Try again.
Enter your guess: 500
Higher! Try again.
Enter your guess: 400 
Higher! Try again.
Enter your guess: 300
Higher! Try again.
Enter your guess: 200
Higher! Try again.
Enter your guess: 100
Higher! Try again.
Enter your guess: 50
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
Siloy-picoctf@webshell:~/drop-in$ ssh -p 56189 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 400
Higher! Try again.
Enter your guess: 300
Higher! Try again.
Enter your guess: 200
Higher! Try again.
Enter your guess: 100
Higher! Try again.
Enter your guess: 50
Higher! Try again.
Enter your guess: 30
Higher! Try again.
Enter your guess: 40
Higher! Try again.
Enter your guess: 42
Higher! Try again.
Enter your guess: 41
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
Siloy-picoctf@webshell:~/drop-in$ ssh -p 56189 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 1
Higher! Try again.
Enter your guess: 2
Higher! Try again.
Enter your guess: 999
Lower! Try again.
Enter your guess: 222
Higher! Try again.
Enter your guess: 13
Higher! Try again.
Enter your guess: 394
Higher! Try again.
Enter your guess: 395
Higher! Try again.
Enter your guess: 
Please enter a valid number.
Enter your guess: 
Please enter a valid number.
Enter your guess: 1
Higher! Try again.
Enter your guess: 55
Higher! Try again.
Enter your guess: 100   
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
Siloy-picoctf@webshell:~/drop-in$ ssh -p 56189 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 999
Lower! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 600
Lower! Try again.
Enter your guess: 500
Lower! Try again.
Enter your guess: 400
Lower! Try again.
Enter your guess: 300
Congratulations! You guessed the correct number: 300
Here's your flag: picoCTF{g00d_gu355_ee8225d0}
Connection to atlas.picoctf.net closed.
Siloy-picoctf@webshell:~/drop-in$ 
```
