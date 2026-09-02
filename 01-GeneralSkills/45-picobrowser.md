## Descripcion
This website can be rendered only by picobrowser, go and catch the flag!

[http://fickle-tempest.picoctf.net:54409](http://fickle-tempest.picoctf.net:54409/)
## solucion 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ curl -s http://fickle-tempest.picoctf.net:55005/flag -H "User-Agent: picobrowser" | grep pico
         <!-- <strong>Title</strong> --> picobrowser!
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}</code></p>

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$

```

```
picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}
```
## notas adicionales
acceder como picobrowser desde la terminal ya que con otro ... browser ya que con otro cliente no muestra la bandera
## referencias
