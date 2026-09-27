## Descripcion

We have several pages hidden. Can you find the one with the flag? The website is running [here](http://xebec.cylabacademy.net:32826/).

folders folders folders 

## solucion 
```
carpetas carpetas carpetas
buscando por el codigo fuente y en todos los archivos .css y .js


nos encontramos con este 
secret/assets/index.css

que no lleva a nada util pero al poner 

view-source:xebec.cylabacademy.net:30253/secret/

nos encontramos con esto 
|   |
|---|
|<!DOCTYPE html>|
|<html>|
|<head>|
|<title></title>|
|<link rel="stylesheet" href="[hidden/file.css](http://xebec.cylabacademy.net:30253/secret/hidden/file.css)" />|
|</head>|
||
|<body>|
|<h1>Finally. You almost found me. you are doing well</h1>|
|<img src="[https://media1.tenor.com/images/0a6aff9f825af62c05adfbd75039cc7b/tenor.gif?itemid=4648337](https://media1.tenor.com/images/0a6aff9f825af62c05adfbd75039cc7b/tenor.gif?itemid=4648337)" alt="Something Like That GIF - Andy Parksandrecreation Wtf GIFs" style="max-width: 833px; background-color: rgb(151, 121, 85);" width="833" height="937.125">|
|</body>|
|</html>|
||



aqui lo que nos importa es hidden/
haci que se lo agregamos a 

view-source:xebec.cylabacademy.net:30253/secret/hidden/


aqui nos encontramos con esto
|   |
|---|
|<!DOCTYPE html>|
|<html>|
|<head>|
|<title>LOGIN</title>|
|<!-- css -->|
|<link href="[superhidden/login.css](http://xebec.cylabacademy.net:30253/secret/hidden/superhidden/login.css)" rel="stylesheet" />|

lo añadimos claro
view-source:xebec.cylabacademy.net:30253/secret/hidden/superhidden/

bingo
|   |
|---|
|<!DOCTYPE html>|
|<html>|
|<head>|
|<title></title>|
|<link rel="stylesheet" href="[mycss.css](http://xebec.cylabacademy.net:30253/secret/hidden/superhidden/mycss.css)" />|
|</head>|
||
|<body>|
|<h1>Finally. You found me. But can you see me</h1>|
|<h3 class="flag">academy{succ3ss_@h3n1c@10n_e77e3359}</h3>|
|</body>|
|</html>|

```

```
academy{succ3ss_@h3n1c@10n_e77e3359}
```
## notas adicionales

se cansan mis ojos..
## referencias
