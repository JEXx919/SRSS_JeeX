## Descripción

Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://challenge-files.cylabacademy.net/library/a454b00812f80f3ffa4115dc27a9eb78fbfcab841218f5502f7f53ab8d5d7f49/flag.png).

## solución 
```

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/a454b00812f80f3ffa4115dc27a9eb78fbfcab841218f5502f7f53ab8d5d7f49/flag.png
--2026-10-17 23:14:10--  https://challenge-files.cylabacademy.net/library/a454b00812f80f3ffa4115dc27a9eb78fbfcab841218f5502f7f53ab8d5d7f49/flag.png
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.37, 13.226.187.22, 13.226.187.66, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.37|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 21564 (21K) [application/octet-stream]
Saving to: ‘flag.png’

flag.png                      100%[=================================================>]  21.06K  --.-KB/s    in 0.001s

2026-10-17 23:14:12 (19.7 MB/s) - ‘flag.png’ saved [21564/21564]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ file flag.png
flag.png: PNG image data, 700 x 450, 8-bit/color RGB, non-interlaced


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$strings flag.png | grep -iE 'academy'
flag.png: PNG image data, 700 x 450, 8-bit/color RGB, non-interlaced
secret/flag.pngUT
academy{Hiddinng_An_imag3_within_@n_ima9e_c29e4ed9}
secret/flag.pngUT

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$

```

```
academy{Hiddinng_An_imag3_within_@n_ima9e_c29e4ed9}
```
## notas adicionales

## referencias
