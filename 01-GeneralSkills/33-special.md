## Descripcion
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)

Start your instance to see connection details.

## solucion 
```
JeeX7ZaZ-academy@webshell:~$ -p 55354 ctf-player@saturn.picoctf.net
-bash: -p: command not found
JeeX7ZaZ-academy@webshell:~$ ssh -p 55354 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:55354 ([13.59.203.175]:55354)' can't be established.
ED25519 key fingerprint is SHA256:tJ0wuU5yBvNO/FrkHmR9iY36VJClMhKV+Hq2sxqKFmg.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:16: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:55354' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.17.0-1019-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

Special$ /ls 
Absolutely not paths like that, please!
Special$ /../
Absolutely not paths like that, please!
Special$ ../../../../bin/bash
Why go back to an inferior shell?
Special$ /bin/bash
Why go back to an inferior shell?
Special$ ../../../../bin/ls -la
../../../../bin/ls la 
../../../../bin/ls: cannot access 'la': No such file or directory
Special$ Special$ ../../../../bin/ls -la
../../../../bin/ls la 
../../../../bin/ls: cannot access 'la': No such file or directory
Special$ Special ../../../../bin/ls la 
sh: 1: Special: not found
Special$ ../../../../bin/ls la 
../../../../bin/ls: cannot access 'la': No such file or directory
Special$ ../../../../bin/ls: cannot access la's No such file or directory 
sh: 1: Syntax error: Unterminated quoted string
Special$ ../../../../bin/ls   
Special ../../../../bin/ls 
sh: 1: Special: not found
Special$ ../../../../bin/ls
../../../../bin/ls 
blargh
Special$ ../../../../bin/cat blargh
../../../../bin/cat large 
../../../../bin/cat: large: No such file or directory
Special$ ../../../../bin/cat ./blargh
../../../../bin/cat ./blargh 
../../../../bin/cat: ./blargh: Is a directory
Special$ ../../../../bin/ls ./blargh
../../../../bin/ls ./blargh 
flag.txt
Special$ ../../../../bin/blargh/cat ./flag.txt
../../../../bin/blargh/cat ./flag.txt 
sh: 1: ../../../../bin/blargh/cat: not found
Special$ ../../../../bin/cat ./blargh/flag.txt
../../../../bin/cat ./blargh/flag.txt 
picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794}
```

```
picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794}
```
## notas adicionales
Eludimos el corrector, al colocar muchisimo texo

sh: 1: Judo: not found
Special$ Traceback (most recent call last):
  File "/usr/local/Special.py", line 19, in module
    elif cmd[0] == '/':
encontramos esto... y al colocar rutas relativas ../../ y al notar que desde hai se pueden ejecutar comandos damos con la bandera.

## referencias
[Webshell](https://webshell.cylabacademy.org/)
https://gemini.google.com