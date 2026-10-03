## Descripción
Why search for the flag when I can make a bookmarklet to print it for me? Browse [here](http://chatelaine.cylabacademy.net:25027/), and find the flag!

A bookmarklet is a bookmark that runs JavaScript instead of loading a webpage.
What happens when you click a bookmarklet?
Web browsers have other ways to run JavaScript too.



## solución 
![[Pasted image 20261002192509.png]]
```

Codigo Bookmarklet 
javascript:(function() {
            var encryptedFlag = "ÑÌÄÓÈáßëÙ£ÖÓÚåÛÑ¢ÕÓÌ¡ ¬í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
        
    


Un **bookmarklet** es un marcador del navegador que guarda **código JavaScript**
y se puede ejecutar desde el modo desarrollador (F12) desde el apartado consola.
En navegadores actuales muestran un mensaje como este... 
```
![[Pasted image 20261002194046.png]]
```
En navegadores actuales muestran un mensaje como este... 
aunque si escribes 

allow pasting

y das Enter te permitira ejecutar el codigo.
```

![[Pasted image 20261002194238.png]]
![[Pasted image 20261002200433.png]]

```
Y al ejecutarlo...

obtenemos una bandera erronea.

si buscamos dentro del codigo fuente de la pajina y obtenemos este codigo.
|   |
|---|
|javascript:(function() {|
|var encryptedFlag = "ÑÌÄÓÈáßëÙ£ÖÓÚåÛÑ¢ÕÓÌ¡ ¬í";|
|var key = "picoctf";|
|var decryptedFlag = "";|
|for (var i = 0; i < encryptedFlag.length; i++) {|
|decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);|
|}|
|alert(decryptedFlag);|
|})();|

y lo ejecutamos... nuevamente obtenemos una bandera que no sirve.

```
![[Pasted image 20261002201229.png]]





///////////////////////////////
actualización, quizás los de cylab corrigieron el error... desconozco que hacia que la llave fuese ilegible y incorrecta


![[Pasted image 20261003155910.png]]


```
academy{p@g3_turn3r_f1291985}
```
## notas adicionales


 
## referencias

[Bookmarklet - Wikipedia](https://en.wikipedia.org/wiki/Bookmarklet)