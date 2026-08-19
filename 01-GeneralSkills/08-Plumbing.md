
## Descripcion
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ nc fickle-tempest.picoctf.net 54474 > H
^C  
JeeX7ZaZ-academy@webshell:~$ ls
H  README.txt  file  flag  hola  holal  ter
JeeX7ZaZ-academy@webshell:~$ cat h | grep pico
cat: h: No such file or directory
JeeX7ZaZ-academy@webshell:~$ cat H | grep pico
picoCTF{digital_plumb3r_00da27CC}
JeeX7ZaZ-academy@webshell:~$ 
```

```
picoCTF{digital_plumb3r_00da27CC}
```
## notas adicionales

Nos conectamos al servidor desde la consola y todo lo que el servidor mande de respuesta lo colocamos en una archivo en este caso H, ya solo con cat y grep buscamos la bandera

## referencias
[Webshell](https://webshell.cylabacademy.org/)