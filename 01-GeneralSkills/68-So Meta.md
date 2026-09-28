## Descripcion
Find the flag in this [picture](https://challenge-files.cylabacademy.net/library/8179732d3bcbaaf9dadfc7fe08aa5b7fbf1d3189b0a2dc90eca34dca38a85b4a/pico_img.png).

What does meta mean in the context of files?
Ever heard of metadata?
## solucion 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ exiftool pico_img.png
ExifTool Version Number         : 13.55
File Name                       : pico_img.png
Directory                       : .
File Size                       : 109 kB
File Modification Date/Time     : 2026:09:22 19:49:08-06:00
File Access Date/Time           : 2026:09:28 10:45:21-06:00
File Inode Change Date/Time     : 2026:09:28 10:45:05-06:00
File Permissions                : -rw-r--r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Artist                          : academy{s0_m3ta_45015e26}
Image Size                      : 600x600
Megapixels                      : 0.360










ver solo un metadato

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ exiftool -Artist pico_img.png
Artist                          : academy{s0_m3ta_45015e26}


```

```
academy{s0_m3ta_45015e26}
```
## notas adicionales


como usar exiftool para meter un codigo php en un metadato... (investigar)
## referencias
