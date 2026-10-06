## Descripción
We found this [packet capture](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key). Recover the flag.

Try using a tool like Wireshark.
## solución 

![[Pasted image 20261005215241.png]]





```

creamos una carpeta para el reto y bajamos los archivos
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ mkdir WebNet0

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ls
WebNet0

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cd WebNet0

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/WebNet0]
└─$ wget https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap
--2026-10-05 15:41:27--  https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.66, 13.226.187.37, 13.226.187.22, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13163 (13K) [application/octet-stream]
Saving to: ‘webnet0-capture.pcap’

webnet0-capture.pcap                         100%[==============================================================================================>]  12.85K  --.-KB/s    in 0s

2026-10-05 15:41:28 (46.1 MB/s) - ‘webnet0-capture.pcap’ saved [13163/13163]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~/WebNet0]
└─$ wget https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key
--2026-10-05 15:41:41--  https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.66, 13.226.187.40, 13.226.187.37, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key                                 100%[==============================================================================================>]   1.66K  --.-KB/s    in 0s

2026-10-05 15:41:42 (27.7 MB/s) - ‘picopico.key’ saved [1704/1704]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~/WebNet0]
└─$ wireshark webnet0-capture.pcap &
[1] 4335


no encontramos nada usando filtros ni busqueda.
cambiamos protocols lelndo a

edit - preferences - protocols - seleccionamos TLS y editamos la RSA key list
y en key file añadimos el archivo que descargamos con extencion .key
y dejamos los demas campos en blanco... damos ok a todo y salimos y volvemos a entrar.

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/WebNet0]
└─$ wireshark webnet0-capture.pcap &
[2] 4447
[1]   Done                       wireshark webnet0-capture.pcap

```


Colocamos en el filtro http y en los paquetes que quedan les damos clic derecho 
-Follow y damos clic en TLS Stream
esto nos mostrara una pestaña como esta, será cuestión de hacer eso con los paquetes hasta dar con la bandera...
![[Pasted image 20261005215728.png]]

o bien se puede hacer uso del buscador 
![[Pasted image 20261005221023.png]]
```
academy{nongshim.shrimp.crackers}
```
## notas adicionales

## referencias
