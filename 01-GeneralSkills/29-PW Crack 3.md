## Descripcion
Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.

There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/16/level3.py
--2026-08-27 05:34:50--  https://artifacts.picoctf.net/c/16/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.64, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                       100%[=====================================================================================================>]   1.31K  --.-KB/s    in 0s      

2026-08-27 05:34:50 (572 MB/s) - 'level3.py' saved [1337/1337]

JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
--2026-08-27 05:35:01--  https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc                             100%[=====================================================================================================>]      31  --.-KB/s    in 0s      

2026-08-27 05:35:01 (331 KB/s) - 'level3.flag.txt.enc' saved [31/31]

JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/16/level3.hash.bin
--2026-08-27 05:35:12--  https://artifacts.picoctf.net/c/16/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin                                 100%[=====================================================================================================>]      16  --.-KB/s    in 0s      

2026-08-27 05:35:12 (800 KB/s) - 'level3.hash.bin' saved [16/16]

JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ ls  
level3.flag.txt.enc  level3.hash.bin  level3.py
JeeX7ZaZ-academy@webshell:~$ cat -l level3.py
cat: invalid option -- 'l'
Try 'cat --help' for more information.
JeeX7ZaZ-academy@webshell:~$ nano -l level3.py
JeeX7ZaZ-academy@webshell:~$ "6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"
-bash: 6997,: command not found
JeeX7ZaZ-academy@webshell:~$ python3 level3.py
Please enter correct password for flag: 6997
That password is incorrect
JeeX7ZaZ-academy@webshell:~$ python3 level3.py
Please enter correct password for flag: 3ac8
That password is incorrect
JeeX7ZaZ-academy@webshell:~$ python3 level3.py
Please enter correct password for flag: f0ac
That password is incorrect
JeeX7ZaZ-academy@webshell:~$ python3 level3.py
Please enter correct password for flag: 4b17
That password is incorrect
JeeX7ZaZ-academy@webshell:~$ python3 level3.py
Please enter correct password for flag: ec27
That password is incorrect
JeeX7ZaZ-academy@webshell:~$ python3 level3.py
Please enter correct password for flag: 4e66
That password is incorrect
JeeX7ZaZ-academy@webshell:~$ python3 level3.py
Please enter correct password for flag: 865e
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
JeeX7ZaZ-academy@webshell:~$ 
```

```
picoCTF{m45h_fl1ng1ng_2b072a90}
```
## notas adicionales

descargue todos los archivos y al abrir el script de python este al final menciona que la contraseña es una de 7 posibles... así que probé todas
## referencias
