## Descripción
Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/bb0cb9b59f754a578fdcff72400d49394fe4399b5bf0d34f650c5baffbad8575/disk.flag.img.gz)
## solución 
```
mkdir operation_orchid

cd operation_orchid

wget https://challenge-files.cylabacademy.net/library/bb0cb9b59f754a578fdcff72400d49394fe4399b5bf0d34f650c5baffbad8575/disk.flag.img.gz

disk.flag.img.gz

gunzip disk.flag.img.gz 

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/operation_orchid]
└─$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/operation_orchid]
└─$ fls -o 411648 disk.flag.img -r | grep flag
+ r/r * 1876(realloc):  flag.txt
+ r/r 1782:     flag.txt.enc

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/operation_orchid]
└─$ fls -o 411648 disk.flag.img -r | grep flag -A 2 -B 2
d/d 472:        root
+ r/r 1875:     .ash_history
+ r/r * 1876(realloc):  flag.txt
+ r/r 1782:     flag.txt.enc
d/d 473:        run
d/d 475:        srv

ubicamos que se encuentra en root

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/operation_orchid]
└─$ icat -o 411648 disk.flag.img 1782
Salted__
CM�<�@�����x�
vS����۸�ߚQ��#�t�C5uȤ7� ���؎$�'%

encriptado ssl 

veremos el archivo .ash.history
┌──(jeex㉿LAPTOP-77F4GRAK)-[~/operation_orchid]
└─$ icat -o 411648 disk.flag.img 1875
touch flag.txt
nano flag.txt
apk get nano
apk --help
apk add nano
nano flag.txt
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt


icat icat -o 411648 disk.flag.img 1782 > fag.txt.enc

file flag.txt.enc

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/operation_orchid]
└─$ cat fag.txt.enc
Salted__
CM�<�@�����x�
vS����۸�ߚQ��#�t�C5uȤ7� ���؎$�'%


icat -o 411648 disk.flag.img.gz 1875

se uso el algoritmo aes256 y ai mismo encontramos el password


-- no hacemos esto..
copaeamos el comando y cambiamos la entrada y la salida... //o mejor 
---

invertir entrada y salida 
copeamos el comando de encriptacion cambiamos el archivo de encitacion y encriptado y colocamos -d al final

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/operation_orchid]
└─$ openssl aes256 -salt -in fag.txt.enc -out flag.txt -k unbreakablepassword1234567 -d
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
404768DEAE7D0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:

cat flag.txt


┌──(jeex㉿LAPTOP-77F4GRAK)-[~/operation_orchid]
└─$ cat flag.txt
academy{h4un71ng_p457_0b36d810}







```

```
academy{h4un71ng_p457_0b36d810}
```
## notas adicionales

## referencias
