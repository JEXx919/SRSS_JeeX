## Descripcion
Our flag printing service has started glitching!
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ nc saturn.picoctf.net 51544
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
^C
JeeX7ZaZ-academy@webshell:~$ python
Python 3.10.12 (main, Mar  3 2026, 11:56:32) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
KeyboardInterrupt
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
'picoCTF{gl17ch_m3_n07_bda68f75}'
```

```
picoCTF{gl17ch_m3_n07_bda68f75}
```
## notas adicionales
Abrir el puerto del servidor y mandara la bandera, pero sin teriminar y con ayuda de python traducimos la bandera.
## referencias
[Webshell](https://webshell.cylabacademy.org/)