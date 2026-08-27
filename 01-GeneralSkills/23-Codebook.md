## Descripcion
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)


On the webshell, use `ls` to see if both files are in the directory you are in.

The `str_xor` function does not need to be reverse engineered for this challenge.
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/3/code.py
--2026-08-27 04:53:37--  https://artifacts.picoctf.net/c/3/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.64, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                         100%[=====================================================================================================>]   1.25K  --.-KB/s    in 0s      

2026-08-27 04:53:37 (591 MB/s) - 'code.py' saved [1278/1278]

JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/3/codebook.txt
--2026-08-27 04:53:49--  https://artifacts.picoctf.net/c/3/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                    100%[=====================================================================================================>]      27  --.-KB/s    in 0s      

2026-08-27 04:53:49 (18.9 MB/s) - 'codebook.txt' saved [27/27]


JeeX7ZaZ-academy@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_197a982c}
```

```
picoCTF{c0d3b00k_455157_197a982c}
```
## notas adicionales
descargar ambos archivos y ejecutar el archivo .py era necesario que el archivo .txt existiera en el directorio.

## referencias
[Webshell](https://webshell.cylabacademy.org/)