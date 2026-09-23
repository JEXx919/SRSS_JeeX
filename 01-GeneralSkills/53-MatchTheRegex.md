## Descripcion
How about trying to match a regular expression

The website is running [here](http://saturn.picoctf.net:52565/).

  
Access the webpage and try to match the regular expression associated with the text field
## solucion 
```
colocar picoCTF y presionar submit
|   |
|---|
|<script>|
|function send_request() {|
|let val = document.getElementById("name").value;|
|// ^p.....F!?|
|fetch(`/flag?input=${val}`)|
|.then(res => res.text())|
|.then(res => {|
|const res_json = JSON.parse(res);|
|alert(res_json.flag)|
|return false;|
|})|
|return false;|
|}|
||
|</script>|
```

```
picoCTF{succ3ssfully_matchtheregex_2375af79}
```
## notas adicionales
hacer que coincida el texto que subimos a la pagina web con la expresión regular que solo es que comience con (p) y termine en (F) y habiendo 5 caracteres entre estas dos letras o colocamos picoCTF
## referencias
[RegExr: Learn, Build, & Test RegEx](https://regexr.com/)