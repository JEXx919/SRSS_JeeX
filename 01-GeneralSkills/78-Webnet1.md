## Descripción

We found this [packet capture](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/webnet1-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/picopico.key). Recover the flag.
  
Try using a tool like Wireshark.
How can you decrypt the TLS stream?
## solución 
```
crear una carpeta para el reto, bajar los archivos, y brir el archivo con wireshark
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ mkdir Webnet1

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cd Webnet1

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/Webnet1]
└─$ wget https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/webnet1-capture.pcap
--2026-10-05 22:17:34--  https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/webnet1-capture.pcap
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.37, 13.226.187.22, 13.226.187.66, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.37|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92525 (90K) [application/octet-stream]
Saving to: ‘webnet1-capture.pcap’

webnet1-capture.pcap                         100%[==============================================================================================>]  90.36K  --.-KB/s    in 0.1s

2026-10-05 22:17:35 (909 KB/s) - ‘webnet1-capture.pcap’ saved [92525/92525]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~/Webnet1]
└─$ wget https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/picopico.key
--2026-10-05 22:17:46--  https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/picopico.key
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.66, 13.226.187.40, 13.226.187.37, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key                                 100%[==============================================================================================>]   1.66K  --.-KB/s    in 0s

2026-10-05 22:17:47 (34.1 MB/s) - ‘picopico.key’ saved [1704/1704]

```

Al protocol TLS le añadimos el archivo picopico.key al key file
![[Pasted image 20261005222022.png]]
Preferences
![[Pasted image 20261005222057.png]]
Protocols - TLS - RSA keyS list
![[Pasted image 20261005222143.png]]
Añadimos el archivo
![[Pasted image 20261005222234.png]]
Damos ok a todo y cerramos el programa y abrimos nuevamente(creo que esto no se ocupa realmente... pero pues mejor hacerlo)

En filtro colocamos http.
Con ayuda del buscador, colocando Strings y Packet details damos con el archivo de la que contiene la bandera
![[Pasted image 20261005222519.png]]
Clic derecho sobre el.
![[Pasted image 20261005222621.png]]
Presionamos Follow y luego seleccionamos TLS Stream
![[Pasted image 20261005222659.png]]
Encontramos la bandera.
![[Pasted image 20261005222736.png]]


Y pues nos... 
Nos vamos a File 
![[Pasted image 20261005224813.png]]

![[Pasted image 20261005224903.png]]

y guardamos esa imagen...
```

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/Webnet1]
└─$ ls
picopico.key  vulture.jpg  webnet1-capture.pcap

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/Webnet1]
└─$ open vulture.jpg
```


![[Pasted image 20261005224950.png]]
... bastantes bromas

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~/Webnet1]
└─$ exiftool vulture.jpg
ExifTool Version Number         : 13.55
File Name                       : vulture.jpg
Directory                       : .
File Size                       : 70 kB
File Modification Date/Time     : 2026:10:05 22:48:54-06:00
File Access Date/Time           : 2026:10:05 22:49:28-06:00
File Inode Change Date/Time     : 2026:10:05 22:48:54-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Exif Byte Order                 : Big-endian (Motorola, MM)
X Resolution                    : 1
Y Resolution                    : 1
Resolution Unit                 : None
Artist                          : academy{honey.roasted.peanuts}
Y Cb Cr Positioning             : Centered
Profile CMM Type                : Little CMS
Profile Version                 : 2.1.0
Profile Class                   : Display Device Profile
Color Space Data                : RGB
Profile Connection Space        : XYZ
Profile Date Time               : 2012:01:25 03:41:57
Profile File Signature          : acsp
Primary Platform                : Apple Computer Inc.
CMM Flags                       : Not Embedded, Independent
Device Manufacturer             :
Device Model                    :
Device Attributes               : Reflective, Glossy, Positive, Color
Rendering Intent                : Perceptual
Connection Space Illuminant     : 0.9642 1 0.82491
Profile Creator                 : Little CMS
Profile ID                      : 0
Profile Description             : c2
Profile Copyright               : FB
Media White Point               : 0.9642 1 0.82491
Media Black Point               : 0.01205 0.0125 0.01031
Red Matrix Column               : 0.43607 0.22249 0.01392
Green Matrix Column             : 0.38515 0.71687 0.09708
Blue Matrix Column              : 0.14307 0.06061 0.7141
Red Tone Reproduction Curve     : (Binary data 64 bytes, use -b option to extract)
Green Tone Reproduction Curve   : (Binary data 64 bytes, use -b option to extract)
Blue Tone Reproduction Curve    : (Binary data 64 bytes, use -b option to extract)
Image Width                     : 640
Image Height                    : 716
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 640x716
Megapixels                      : 0.458

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/Webnet1]
└─$
```



```
academy{honey.roasted.peanuts}
```
## notas adicionales

## referencias
