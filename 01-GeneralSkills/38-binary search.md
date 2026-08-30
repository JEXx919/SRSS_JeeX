## Descripcion
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.

Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!

You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ ssh -p 52350 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Lower! Try again.
Enter your guess: 625
Higher! Try again.
Enter your guess: 687
Lower! Try again.
Enter your guess: 656
Higher! Try again.
Enter your guess: 671
Higher! Try again.
Enter your guess: 679
Lower! Try again.
Enter your guess: 675
Lower! Try again.
Enter your guess: 673
Lower! Try again.
Enter your guess: 672
Congratulations! You guessed the correct number: 672
Here's your flag: picoCTF{g00d_gu355_3af33d18}
Connection to atlas.picoctf.net closed.
JeeX7ZaZ-academy@webshell:~$ 

```

```
picoCTF{g00d_gu355_3af33d18}
```
## notas adicionales


Aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa ir buscando formando intervalos y colocando la mitad de los intervalos para seguir obteniendo parejas de números y  colocando la mitas.

se puede automatizar con un scrip de python??? si


## referencias
