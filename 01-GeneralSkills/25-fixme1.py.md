## Descripcion
Fix the syntax error in this Python script to print the flag.
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/26/fixme1.py
--2026-08-27 05:06:15--  https://artifacts.picoctf.net/c/26/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                       100%[=====================================================================================================>]     837  --.-KB/s    in 0s      

2026-08-27 05:06:15 (453 MB/s) - 'fixme1.py' saved [837/837]

JeeX7ZaZ-academy@webshell:~$ python3 fixme1.py
  File "/home/JeeX7ZaZ-academy/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent

JeeX7ZaZ-academy@webshell:~$ nano -l fixme1.py
JeeX7ZaZ-academy@webshell:~$ python3 fixme1repared.py
```

```
picoCTF{1nd3nt1ty_cr1515_09ee727a}
```
## notas adicionales
corregir el error de Python, una lineal no estaba bien identada
## referencias
[Webshell](https://webshell.cylabacademy.org/)