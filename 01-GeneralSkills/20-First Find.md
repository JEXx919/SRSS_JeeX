## Descripcion
Unzip this archive and find the file named 'uber-secret.txt'
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/500/files.zip
--2026-08-24 20:27:15--  https://artifacts.picoctf.net/c/500/files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3995553 (3.8M) [application/octet-stream]
Saving to: 'files.zip'

files.zip                                       100%[=====================================================================================================>]   3.81M  1.83MB/s    in 2.1s    

2026-08-24 20:27:17 (1.83 MB/s) - 'files.zip' saved [3995553/3995553]

JeeX7ZaZ-academy@webshell:~$ ls
files.zip
JeeX7ZaZ-academy@webshell:~$ unzip files.zip
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
JeeX7ZaZ-academy@webshell:~$ ls
files  files.zip


SOLUCION 1
eeX7ZaZ-academy@webshell:~$ cd files
JeeX7ZaZ-academy@webshell:~/files$ cd adequate_books
JeeX7ZaZ-academy@webshell:~/files/adequate_books$ cd more_books
JeeX7ZaZ-academy@webshell:~/files/adequate_books/more_books$ cd .secret
JeeX7ZaZ-academy@webshell:~/files/adequate_books/more_books/.secret$ cd deeper_secrets
JeeX7ZaZ-academy@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets$ cd deepest_secrets
JeeX7ZaZ-academy@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ ls 
uber-secret.txt
JeeX7ZaZ-academy@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ cat uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}


SOLUCION 2

JeeX7ZaZ-academy@webshell:~$ grep -r "pico" files/
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}
files/14789.txt.utf-8:brassa un picotin d'orge_. Comme depuis une demi-heure environ c'était
JeeX7ZaZ-academy@webshell:~$ 

```

```
picoCTF{f1nd_15_f457_ab443fd1}
```
## notas adicionales

bajar el archivo y descomprimirlo dirijirse al directorio del archivo de forma manual o con uso de un grep recursivo buscar la bandera entre todos los archivos. 
## referencias
[Webshell](https://webshell.cylabacademy.org/)
grep --help
-r, --recursive           like --directories=recurse
https://gemini.google.com/