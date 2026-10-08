## Descripción

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.cylabacademy.net/library/cb4d1ac86836c86e1ea16a4be1d8cf72c0465c6edcc0ab886728040a28dd7966/dds1-alpine.flag.img.gz)


  
Have you ever used `file` to determine what a file was?

Relevant terminal-fu in Challenge Library: [https://learn.cylabacademy.org/library/85](https://learn.cylabacademy.org/library/85)

Mastering this terminal-fu would enable you to find the flag in a single command: [https://learn.cylabacademy.org/library/48](https://learn.cylabacademy.org/library/48)

Using your own computer, you could use qemu to boot from this disk!
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ mkdir slew

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cd slew

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/slew]
└─$ wget https://challenge-files.cylabacademy.net/library/cb4d1ac86836c86e1ea16a4be1d8cf72c0465c6edcc0ab886728040a28dd7966/dds1-alpine.flag.img.gz
--2026-10-07 10:57:04--  https://challenge-files.cylabacademy.net/library/cb4d1ac86836c86e1ea16a4be1d8cf72c0465c6edcc0ab886728040a28dd7966/dds1-alpine.flag.img.gz
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.66, 13.226.187.22, 13.226.187.40, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768910 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img.gz       100%[=================================================>]  28.39M  1.71MB/s    in 22s

2026-10-07 10:57:28 (1.30 MB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768910/29768910]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~/slew]
└─$ gzip -d dds1-alpine.flag.img.gz

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/slew]
└─$ ls
dds1-alpine.flag.img

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/slew]
└─$ ls -lah
total 129M
drwxr-xr-x  2 jeex jeex 4.0K Oct  7 10:59 .
drwx------ 11 jeex jeex  32K Oct  7 10:56 ..
-rw-r--r--  1 jeex jeex 128M Sep 22 20:21 dds1-alpine.flag.img


┌──(jeex㉿LAPTOP-77F4GRAK)-[~/slew]
└─$ file dds1-alpine.flag.img
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors


┌──(jeex㉿LAPTOP-77F4GRAK)-[~/slew]
└─$ open dds1-alpine.flag.img

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/slew]
└─$ srch_strings dds1-alpine.flag.img | grep academy
  SAY academy{f0r3ns1c4t0r_n30phyt3_6502313d}
```

```
academy{f0r3ns1c4t0r_n30phyt3_6502313d}
```
## notas adicionales

## referencias
