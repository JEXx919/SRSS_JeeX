## Descripción
🥛

Look at the problem category
## solución 
```

zsteg -a
lsb 


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget http://chatelaine.cylabacademy.net:30785/concat_v.png
--2026-10-07 23:18:17--  http://chatelaine.cylabacademy.net:30785/concat_v.png
Resolving chatelaine.cylabacademy.net (chatelaine.cylabacademy.net)... 18.227.187.235
Connecting to chatelaine.cylabacademy.net (chatelaine.cylabacademy.net)|18.227.187.235|:30785... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18095896 (17M) [image/png]
Saving to: ‘concat_v.png’

concat_v.png                  100%[=================================================>]  17.26M  2.12MB/s    in 11s

2026-10-07 23:18:28 (1.58 MB/s) - ‘concat_v.png’ saved [18095896/18095896]



┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ RUBY_THREAD_VM_STACK_SIZE=50000000 zsteg concat_v.png
imagedata           .. text: "\n\n\n\n\n\n\t\t"
chunk:0:IHDR        .. file: Adobe Photoshop Color swatch, version 0, 1280 colors; 1st RGB space (0), w 0xb9a0, x 0x802, y 0, z 0; 2nd RGB space (0), w 0, x 0, y 0, z 0
b1,b,lsb,xy         .. text: "academy{imag3_m4n1pul4t10n_sl4p5}\n"
b1,bgr,lsb,xy       .. <wbStego size=0xb4125b ext=nil data="\x126I\xB7\x7F\xDFl[\xB6>\x7F\xDF\x86\x7F\xB7c\xFCI\x13\xDFwZr\xE4V\x91\xE5\x12\xD8\x0E\e\xE5&MR[\xB2\xDB:\xB5\xBFo\xDB\xF6\xDB\xF7\x12\x04\bm\xDB\xB6m\xDB\xB6\x00\x00\x00m\xB6m\xDB\xB6m\xDB\x00\x00\x00\xB6m\xDB\x00m\xDBI\x92\x12m\xDB\xB6\x00\x00\x00\x00\x00\x00m\xDB\xB6\xDB\x00m\xDB\x00\x00\x00\xB6m\xDB\xB6m\xDB\xB6m\xB6\x00\x00\x00\x00\x00\x00m\xDB" even=true hdr=nil enc=nil mix=true controlbyte="[">
b2,r,lsb,xy         .. text: ["U" repeated 8 times]
b2,r,msb,xy         .. file: VISX image file
b2,g,lsb,xy         .. file: VISX image file
b2,g,msb,xy         .. file: SoftQuad DESC or font file binary - version 15722
b2,b,msb,xy         .. text: "UfUUUU@UUU"
b4,r,lsb,xy         .. text: "\"\"\"\"\"#4D"
b4,r,msb,xy         .. text: "wwww3333"
b4,g,lsb,xy         .. text: "wewwwwvUS"
b4,g,msb,xy         .. text: "\"\"\"\"DDDD"
b4,b,lsb,xy         .. text: "TTC#23#!"
b4,b,msb,xy         .. text: "UUYYUUUUUUUU"




///tambien 
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ RUBY_THREAD_VM_STACK_SIZE=50000000 zsteg -a concat_v.png | grep academy
b1,b,lsb,xy         .. text: "academy{imag3_m4n1pul4t10n_sl4p5}\n"


```

```
```
## notas adicionales

## referencias
