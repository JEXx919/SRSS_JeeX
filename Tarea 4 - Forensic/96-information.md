## Descripción

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg)

Look at the details of the file

Make sure to submit the flag as academy{XXXXX}
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg
--2026-10-17 23:03:35--  https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.37, 13.226.187.66, 13.226.187.40, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.37|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 878136 (858K) [application/octet-stream]
Saving to: ‘cat.jpg’

cat.jpg                       100%[=================================================>] 857.55K   278KB/s    in 3.1s

2026-10-17 23:03:39 (278 KB/s) - ‘cat.jpg’ saved [878136/878136]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ exiftool cat.jpg
ExifTool Version Number         : 13.55
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2026:09:22 20:44:41-06:00
File Access Date/Time           : 2026:10:17 23:03:39-06:00
File Inode Change Date/Time     : 2026:10:17 23:03:39-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 13.25
License                         : YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1




YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9

From Base64
academy{the_m3tadata_1s_modified}


```

```
academy{the_m3tadata_1s_modified}
```
## notas adicionales

## referencias
[From Base64 - CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=WVdOaFpHVnRlWHQwYUdWZmJUTjBZV1JoZEdGZk1YTmZiVzlrYVdacFpXUjk)