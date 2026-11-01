## Descripción
Hi, intrepid investigator! 📄🔍 You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense. But beware! Not everything is as it appears. Amidst the chaos lies a hidden treasure—an elusive flag waiting to be uncovered. Find the PDF file here [Hidden Confidential Document](https://challenge-files.cylabacademy.net/library/f1a59c8fe4c030bdcdce963b06148196c62afa61f1e959134cd5b547347fddaf/confidential.pdf) and uncover the flag within the metadata.

Don't be fooled by the visible text; it’s just a decoy!

Look beyond the surface for hidden clues
## solución 
**1. Usar ExifTool (Recomendado)** Ejecuta el siguiente comando para revelar toda la información oculta del archivo: `exiftool confidential.pdf` Revisa la lista de resultados. La bandera suele estar guardada en campos como "Title", "Author".
```
ExifTool Version Number         : 13.55
File Name                       : confidential.pdf
Directory                       : .
File Size                       : 183 kB
File Modification Date/Time     : 2026:09:23 00:28:06-06:00
File Access Date/Time           : 2026:10:31 19:36:09-06:00
File Inode Change Date/Time     : 2026:10:31 19:36:09-06:00
File Permissions                : -rw-r--r--
File Type                       : PDF
File Type Extension             : pdf
MIME Type                       : application/pdf
PDF Version                     : 1.7
Linearized                      : No
Page Count                      : 1
Producer                        : PyPDF2
Author                          : YWNhZGVteXtwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV8zY2M3Y2VhOX0=



```
El author esta codificado en base 64, ahi se encuentra nuestra bandera. Decodificar la bandera que se encuentra en base64
```
```
## notas adicionales

## referencias


[From Base64 - CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=WVdOaFpHVnRlWHR3ZFhwNmJETmtYMjB6ZEdGa1lYUmhYMll3ZFc1a0lWOHpZMk0zWTJWaE9YMD0)