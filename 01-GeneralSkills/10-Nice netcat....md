## Descripcion
There is a nice program that you can talk to by using this command in a shell:

1 You can practice using netcat with this picoGym problem: what's a netcat?

2 You can practice reading and writing ASCII with this picoGym problem: Let's Warm Up
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ nc wily-courier.picoctf.net 54016
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
100 
57 
52 
55 
54 
125 
10 

```

```
picoCTF{g00d_k1tty!_n1c3_k1tty!_d9476}
```
## notas adicionales
El servidor al que nos conectamos manda una serie de numeros y haciendo uso de una herramienta llamada cybercheff pasamos esos numeros con from decimal y obtenemos la bandera

## referencias
[From Decimal - CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Decimal\('Space',false\)&input=MTEyIA0KMTA1IA0KOTkgDQoxMTEgDQo2NyANCjg0IA0KNzAgDQoxMjMgDQoxMDMgDQo0OCANCjQ4IA0KMTAwIA0KOTUgDQoxMDcgDQo0OSANCjExNiANCjExNiANCjEyMSANCjMzIA0KOTUgDQoxMTAgDQo0OSANCjk5IA0KNTEgDQo5NSANCjEwNyANCjQ5IA0KMTE2IA0KMTE2IA0KMTIxIA0KMzMgDQo5NSANCjEwMCANCjU3IA0KNTIgDQo1NSANCjU0IA0KMTI1IA0KMTAg&ieol=CRLF)

[Webshell](https://webshell.cylabacademy.org/)