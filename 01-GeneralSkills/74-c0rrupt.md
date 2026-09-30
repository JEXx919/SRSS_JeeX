## Descripcion
We found this [file](https://challenge-files.cylabacademy.net/library/8388ecc430588d15064755583476bec46e23d42a6d8de6e8995c19e40f2e4c58/c0rrupt-mystery). Recover the flag.

Try fixing the file header
## solucion 
```



┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ xxd -l 120 c0rrupt-mystery
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 aa00 1625 0000 1625 0138  ..pHYs...%...%.8
00000050: d82c 82aa aaff a5ab 4445 5478 5eec 9d6d  .,......DETx^..m
00000060: 96e3 488e 6c67 21f3 f3ed 538b abf5 680d  ..H.lg!...S...h.
00000070: 7c53 8192 a5c9 0c00                      |S......

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ printf '\x00\x00\xff\xa5\x49\x44\x41\x54' | dd of=c0rrupt-mystery bs=1 seek=83 count=8 conv=notrunc
8+0 records in
8+0 records out
8 bytes copied, 0.00039713 s, 20.1 kB/s

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ pngcheck c0rrupt-mystery
zlib warning:  different version (expected 1.3.1, using 1.3.2)

OK: c0rrupt-mystery (1642x1095, 24-bit RGB, non-interlaced, static, 96.3%).

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ mv c0rrupt-mystery c0rrupt-mystery.png
xdg-open c0rrupt-mystery.png
Command 'xdg-open' not found, but can be installed with:
sudo apt install xdg-utils



┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ printf '\x89\x50\x4e\x47\x0d\x0a\x1a\x0a' | dd of=c0rrupt-mystery bs=1 seek=0 count=8 conv=notrunc
8+0 records in
8+0 records out
8 bytes copied, 0.00023766 s, 33.7 kB/s

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ xxd c0rrupt-mystery | head -n 1
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4322 4452  .PNG........C"DR

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ pngcheck c0rrupt-mystery
zlib warning:  different version (expected 1.3.1, using 1.3.2)

c0rrupt-mystery:  invalid chunk name "C"DR" (43 22 44 52)
ERROR: c0rrupt-mystery

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ printf '\x49\x48' | dd of=c0rrupt-mystery bs=1 seek=12 count=2 conv=notrunc
2+0 records in
2+0 records out
2 bytes copied, 0.000138468 s, 14.4 kB/s

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ pngcheck c0rrupt-mystery
zlib warning:  different version (expected 1.3.1, using 1.3.2)

c0rrupt-mystery  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERROR: c0rrupt-mystery

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python3 -c "with open('c0rrupt-mystery', 'rb') as f: data = f.read(); data = data.replace(b'\x49\x52\x24\xf0', b'\x38\xd8\x2c\x82', 1); open('c0rrupt-mystery', 'wb').write(data)"

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ pngcheck c0rrupt-mystery
zlib warning:  different version (expected 1.3.1, using 1.3.2)

c0rrupt-mystery  invalid chunk length (too large)
ERROR: c0rrupt-mystery

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ xxd -l 120 c0rrupt-mystery
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 aa00 1625 0000 1625 0138  ..pHYs...%...%.8
00000050: d82c 82aa aaff a5ab 4445 5478 5eec 9d6d  .,......DETx^..m
00000060: 96e3 488e 6c67 21f3 f3ed 538b abf5 680d  ..H.lg!...S...h.
00000070: 7c53 8192 a5c9 0c00                      |S......

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ printf '\x00\x00\xff\xa5\x49\x44\x41\x54' | dd of=c0rrupt-mystery bs=1 seek=83 count=8 conv=notrunc
8+0 records in
8+0 records out
8 bytes copied, 0.00039713 s, 20.1 kB/s

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ pngcheck c0rrupt-mystery
zlib warning:  different version (expected 1.3.1, using 1.3.2)

OK: c0rrupt-mystery (1642x1095, 24-bit RGB, non-interlaced, static, 96.3%).


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ xdg-open c0rrupt-mystery.png
```
![[Pasted image 20260930123241.png]]
```
academy{c0rrupt10n_1847995}
```
## notas adicionales


reparar el archivo png, hace que sus primeros dígitos correspondan con su tipo de archivo,  y reparar diversos detalles que tiene, como la longitud de uno de los chuncks.

## referencias
