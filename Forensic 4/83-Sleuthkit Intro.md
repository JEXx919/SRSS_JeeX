## Descripción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

[Download disk image](https://challenge-files.cylabacademy.net/library/d8718cbbc14dcd9f9aad532a51d7a01b00e1715ca3b1d654dfef687d0b15cbf5/disk.img.gz) Access checker program: `nc xebec.cylabacademy.net 11160`
## solución 
```

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ mkdir sleuthkit

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cd sleuthkit

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/sleuthkit]
└─$ wget https://challenge-files.cylabacademy.net/library/d8718cbbc14dcd9f9aad532a51d7a01b00e1715ca3b1d654dfef687d0b15cbf5/disk.img.gz
--2026-10-07 23:09:15--  https://challenge-files.cylabacademy.net/library/d8718cbbc14dcd9f9aad532a51d7a01b00e1715ca3b1d654dfef687d0b15cbf5/disk.img.gz
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.66, 13.226.187.22, 13.226.187.37, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                   100%[=================================================>]  28.34M  1.91MB/s    in 13s

2026-10-07 23:09:29 (2.13 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/sleuthkit]
└─$ gunzip disk.img.gz


mmls

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/sleuthkit]
└─$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)



┌──(jeex㉿LAPTOP-77F4GRAK)-[~/sleuthkit]
└─$ nc chatelaine.cylabacademy.net 44512
What is the size of the Linux partition in the given disk image?
Length in sectors: 0000202752
0000202752
Great work!
academy{mm15_f7w!}




```

```
academy{mm15_f7w!}
```
## notas adicionales

## referencias
