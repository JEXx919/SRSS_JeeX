## Descripcion
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/a35dc624cfda858ed12a4bce57f832dad3b433bad6cde2b98e25fae4bc8ff760/strings) without running it?
## solucion 
```
Saving to: 'strings'

strings            100%[==============>] 766.04K  1.83MB/s    in 0.4s    

2026-08-24 16:34:45 (1.83 MB/s) - 'strings' saved [784424/784424]
JeeX7ZaZ-academy@webshell:~$ ls -la
total 1956
drwxr-xr-x 2 JeeX7ZaZ-academy JeeX7ZaZ-academy   4096 Aug 24 16:34 .
drwxr-xr-x 3 root             root                 58 Aug 17 16:48 ..
-rw------- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy    194 Aug 19 17:04 .bash_history
-rw-r--r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy    220 Aug 17 16:48 .bash_logout
-rw-r--r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy   3771 Aug 17 16:48 .bashrc
-rw-r--r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy    807 Aug 17 16:48 .profile
-rw------- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy    227 Aug 19 17:28 .python_history
-rw-rw-r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy 289790 Aug 19 17:19 H
-rw-r--r-- 1 root             root               4510 Aug 24 16:31 README.txt
-rw-rw-r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy  14546 Oct 31  2025 file
-rw-rw-r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy     34 Dec 12  2025 flag
-rw-rw-r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy 287597 Aug 19 17:14 hola
-rw-rw-r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy 287018 Aug 19 17:17 holal
-rw-rw-r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy 784424 Nov 14  2025 strings
-rw-rw-r-- 1 JeeX7ZaZ-academy JeeX7ZaZ-academy 288612 Aug 19 17:16 ter
JeeX7ZaZ-academy@webshell:~$ chmod +x strings
JeeX7ZaZ-academy@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_60eA8fdA}

```

```
picoCTF{5tRIng5_1T_60eA8fdA}
```
## notas adicionales

bajar el archivo a la consola darle permisos de ejecucion... y buscamos la lave con strings y grep

Strings sirve para buscar y mostrar texto legible escondido dentro de archivos binarios o no textuales
## referencias

[Webshell](https://webshell.cylabacademy.org/)
