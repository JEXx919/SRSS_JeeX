# what's a net cat?
## Descripcion
nc tutorial
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ nc --help
nc: invalid option -- '-'
usage: nc [-46CDdFhklNnrStUuvZz] [-I length] [-i interval] [-M ttl]
          [-m minttl] [-O length] [-P proxy_username] [-p source_port]
          [-q seconds] [-s sourceaddr] [-T keyword] [-V rtable] [-W recvlimit]
          [-w timeout] [-X proxy_protocol] [-x proxy_address[:port]]
          [destination] [port]
JeeX7ZaZ-academy@webshell:~$ nc fickle-tempest.picoctf.net 64825
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_5c7cC1a9}
```

```
picoCTF{nEtCat_Mast3ry_5c7cC1a9}
```
## notas adicionales

- NC es un aherramienta de red que permite conectarse a un servidor en un puerto especifico 

 - Tambien puedo abrir un puerto tcp o udp en una maquina y luego desde otro conectarme a ese puerto
## Referencias

[Webshell](https://webshell.cylabacademy.org/)