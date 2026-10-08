## Descripción
Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/162bc8bf6dd1abbc5269c16570e170277369a39cf46bdd8d99443e136fabcc5f/disk.flag.img.gz)
## solución 
```

 wget https://challenge-files.cylabacademy.net/library/162bc8bf6dd1abbc5269c16570e170277369a39cf46bdd8d99443e136fabcc5f/disk.flag.img.gz
 
 gunzip disk.flag.img.gz
 
 ls -lah
 
 file disk.flag.img
 
 srch_strings disk.flag.img | grep acamy
 
┌──(jeex㉿LAPTOP-77F4GRAK)-[~/sleuthkit]
└─$  mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
 
 fls -o 2048 disk.flag.img
 
 
 fls -o 360448 disk.flag.img
 
 fls -o 360448 -r disk.flag.img //listado recursivo


dentro de root 
1995
 
 fls -o 360448 -r disk.flag.img 1995 ...
 
 //si aparece con un * al inicio el archivo esta borrado
 
 icat -o 360448 -r disk.flag.img 2082
 icat -o 360448 -r disk.flag.img 2371
 
 ┌──(jeex㉿LAPTOP-77F4GRAK)-[~/sleuthkit]
└─$ icat -o 360448 -r disk.flag.img 2371
academy{by73_5urf3r_85e9b307}
 
 obtenemos la bandera
 
 
 
```

```
academy{by73_5urf3r_85e9b307}
```
## notas adicionales

## referencias
