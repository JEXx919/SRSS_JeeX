## Descripción
How about some hide and seek?

Download this file [here](https://challenge-files.cylabacademy.net/library/db9453955f3bd6e863102fd10b5c3b1e6ce0517e7c648b76d86172eed079e028/unknown.zip).

How can you view the information about the picture?

If something isn't in the expected form, maybe it deserves attention?
## solución 
```

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/db9453955f3bd6e863102fd10b5c3b1e6ce0517e7c648b76d86172eed079e028/unknown.zip
--2026-10-17 23:34:14--  https://challenge-files.cylabacademy.net/library/db9453955f3bd6e863102fd10b5c3b1e6ce0517e7c648b76d86172eed079e028/unknown.zip
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.22, 13.226.187.40, 13.226.187.66, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2252233 (2.1M) [application/octet-stream]
Saving to: ‘unknown.zip’

unknown.zip                   100%[=================================================>]   2.15M   155KB/s    in 12s

2026-10-17 23:34:26 (187 KB/s) - ‘unknown.zip’ saved [2252233/2252233]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ exiftool unknown.zip
ExifTool Version Number         : 13.55
File Name                       : unknown.zip
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2026:09:22 23:17:51-06:00
File Access Date/Time           : 2026:10:17 23:34:26-06:00
File Inode Change Date/Time     : 2026:10:17 23:34:26-06:00
File Permissions                : -rw-r--r--
File Type                       : ZIP
File Type Extension             : zip
MIME Type                       : application/zip
Zip Required Version            : 20
Zip Bit Flag                    : 0
Zip Compression                 : Deflated
Zip Modify Date                 : 2026:09:23 05:17:48
Zip CRC                         : 0xb92ce015
Zip Compressed Size             : 2252053
Zip Uncompressed Size           : 2263734
Zip File Name                   : ukn_reality.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ unzip unknown.zip
Archive:  unknown.zip
  inflating: ukn_reality.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ exiftool ukn_reality.jpg
ExifTool Version Number         : 13.55
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2026:09:22 23:17:47-06:00
File Access Date/Time           : 2026:09:22 23:17:47-06:00
File Inode Change Date/Time     : 2026:10:17 23:36:38-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 12.76
Attribution URL                 : YWNhZGVteXtNRTc0RDQ3QV9ISUREM05fYTgxZDk0MzF9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$



YWNhZGVteXtNRTc0RDQ3QV9ISUREM05fYTgxZDk0MzF9Cg==
from base 64
academy{ME74D47A_HIDD3N_a81d9431}
```

```
academy{ME74D47A_HIDD3N_a81d9431}
```
## notas adicionales

## referencias
