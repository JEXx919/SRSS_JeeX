## Descripcion
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)

Can grep be instructed to look at every file in a directory and its subdirectories?
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/504/big-zip-files.zip
--2026-08-24 20:20:01--  https://artifacts.picoctf.net/c/504/big-zip-files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3182988 (3.0M) [application/octet-stream]
Saving to: 'big-zip-files.zip'

big-zip-files.zip                               100%[=====================================================================================================>]   3.04M  1.83MB/s    in 1.7s    

2026-08-24 20:20:03 (1.83 MB/s) - 'big-zip-files.zip' saved [3182988/3182988]

JeeX7ZaZ-academy@webshell:~$ ls
big-zip-files.zip
JeeX7ZaZ-academy@webshell:~$ unzip big-zip-files.zip
....
....
....

JeeX7ZaZ-academy@webshell:~$ ls
big-zip-files  big-zip-files.zip
JeeX7ZaZ-academy@webshell:~$ grep -r "pico" big-zip-files/
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}



```

```
picoCTF{gr3p_15_m4g1c_ef8790dc}
```
## notas adicionales


grep -r "pico" big-zip-files/

con grep llamamos la herramienta de busqueda
con -r hacemos el proceso recursivo  y colocamos la palabra a buscar seguido del directorio 
con / al final

## referencias
[Webshell](https://webshell.cylabacademy.org/)
grep --help
-r, --recursive           like --directories=recurse
https://gemini.google.com/