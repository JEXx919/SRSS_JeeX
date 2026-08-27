## Descripcion
Fix the syntax error in the Python script to print the flag.
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/6/fixme2.py
--2026-08-27 05:15:16--  https://artifacts.picoctf.net/c/6/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                       100%[=====================================================================================================>]   1.00K  --.-KB/s    in 0s      

2026-08-27 05:15:16 (428 MB/s) - 'fixme2.py' saved [1029/1029]
JeeX7ZaZ-academy@webshell:~$ pytho3 fixme2.py
-bash: pytho3: command not found
JeeX7ZaZ-academy@webshell:~$ python3 fixme2.py
  File "/home/JeeX7ZaZ-academy/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^

JeeX7ZaZ-academy@webshell:~$ nano -l fixme2.py
JeeX7ZaZ-academy@webshell:~$ python3 fixme2_1.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
JeeX7ZaZ-academy@webshell:~$ 

```

```
picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```
## notas adicionales
corregir erro del script solo es colocar la condición correcta ==
## referencias
