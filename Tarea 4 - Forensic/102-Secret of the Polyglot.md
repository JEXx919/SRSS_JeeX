## Descripción
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?

Download the suspicious file [here](https://challenge-files.cylabacademy.net/library/00e64c4ab0a092f8fef0d856d022560edd3e465c62dce1b270d764a99a9c4e1a/flag2of2-final.pdf).

This problem can be solved by just opening the file in different ways

## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget "https://challenge-files.cylabacademy.net/library/00e64c4ab0a092f8fef0d856d022560edd3e465c62dce1b270d764a99a9c4e1a/flag2of2-final.pdf" -O flag2of2-final.pdf
--2026-10-17 23:39:41--  https://challenge-files.cylabacademy.net/library/00e64c4ab0a092f8fef0d856d022560edd3e465c62dce1b270d764a99a9c4e1a/flag2of2-final.pdf
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.22, 13.226.187.40, 13.226.187.66, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2901 (2.8K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf                100%[============================================================>]   2.83K  --.-KB/s    in 0.004s

2026-10-17 23:39:42 (734 KB/s) - ‘flag2of2-final.pdf’ saved [2901/2901]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ file flag2of2-final.pdf
flag2of2-final.pdf: PNG image data, 200 x 40, 4-bit colormap, non-interlaced




┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ xdg-open flag2of2-final.pdf

segunda parte
1n_pn9_&_pdf_241519c6}


display flag2of2-final.pdf

para primera parte

```
![[Pasted image 20261017234421.png]]

```
academy{f1u3n7_1n_pn9_&_pdf_241519c6}
```
## notas adicionales

## referencias
