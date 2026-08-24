## Descripcion
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip
--2026-08-24 17:18:21--  https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.95, 3.160.5.64, 3.160.5.40, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 5166 (5.0K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip                            100%[=====================================================================================================>]   5.04K  --.-KB/s    in 0s      

2026-08-24 17:18:21 (24.1 MB/s) - 'Addadshashanammu.zip' saved [5166/5166]

JeeX7ZaZ-academy@webshell:~$ ls
Addadshashanammu.zip
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ cd Addadshashanammu.zip
-bash: cd: Addadshashanammu.zip: Not a directory
JeeX7ZaZ-academy@webshell:~$ cd 
JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ cd Addadshashanammu.zip /
-bash: cd: too many arguments
JeeX7ZaZ-academy@webshell:~$ strings Addadshashanammu.zip | grep pico
printf("*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}\n");
JeeX7ZaZ-academy@webshell:~$ 



solucion 2

JeeX7ZaZ-academy@webshell:~$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
 extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c  
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
JeeX7ZaZ-academy@webshell:~$ cd A
-bash: cd: A: No such file or directory
JeeX7ZaZ-academy@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
JeeX7ZaZ-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet  fang-of-haynekhtnamet.c
JeeX7ZaZ-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./ fang-of-haynekhtnamet
-bash: ./: Is a directory
JeeX7ZaZ-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
JeeX7ZaZ-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ^C
JeeX7ZaZ-academy@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 
```

```
picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}

solucion 2 
picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
```
## notas adicionales
2 soluciones en la primera hacemos uso de strings y buscamos directamente la bandera
y en la solucion 2 descomprimimos el archivo y al ingresar con ayuda de tab nos dirigimos hasta el fondo del el directorio llegando a un archivo el cual solo ejecutamos y obtenemos la bandera

 
## referencias
[Webshell](https://webshell.cylabacademy.org/)