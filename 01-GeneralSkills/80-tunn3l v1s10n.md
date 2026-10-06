## Descripción
We found this file. Recover the flag. [tunn3l_v1s10n](https://challenge-files.cylabacademy.net/library/3b5add918cb4cf98fa62ef4e05eb8c55c6c9ae547a939c6be992ee3aa656ee69/tunn3l_v1s10n)

  
Weird that it won't display right...
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/3b5add918cb4cf98fa62ef4e05eb8c55c6c9ae547a939c6be992ee3aa656ee69/tunn3l_v1s10n
--2026-10-05 12:40:12--  https://challenge-files.cylabacademy.net/library/3b5add918cb4cf98fa62ef4e05eb8c55c6c9ae547a939c6be992ee3aa656ee69/tunn3l_v1s10n
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.40, 13.226.187.66, 13.226.187.22, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2893454 (2.8M) [application/octet-stream]
Saving to: ‘tunn3l_v1s10n’

tunn3l_v1s10n                 100%[=================================================>]   2.76M  2.08MB/s    in 1.3s

2026-10-05 12:40:14 (2.08 MB/s) - ‘tunn3l_v1s10n’ saved [2893454/2893454]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ file tunn3l_v1s10n
tunn3l_v1s10n: data


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ xxd tunn3l_v1s10n | head
00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........
00000010: 0000 6e04 0000 3201 0000 0100 1800 0000  ..n...2.........
00000020: 0000 5826 2c00 c40e 0000 c40e 0000 0000  ..X&,...........
00000030: 0000 0000 0000 2828 4228 2842 2828 4228  ......((B((B((B(
00000040: 2842 2828 4228 2842 2828 4228 2842 2828  (B((B((B((B((B((
00000050: 4228 2842 2828 4228 2842 2828 4228 2842  B((B((B((B((B((B
00000060: 2828 4228 2842 2828 4228 2842 2828 4228  ((B((B((B((B((B(
00000070: 2842 2828 4228 2842 2828 4228 2842 2828  (B((B((B((B((B((
00000080: 4228 2842 2828 4228 2842 2828 4228 2842  B((B((B((B((B((B
00000090: 2828 4228 2842 2828 4228 2842 2828 4228  ((B((B((B((B((B(



nano reparar.py
# Abrimos el archivo original en modo lectura binaria ('rb')
with open("tunn3l_v1s10n", "rb") as f:
    # bytearray nos permite modificar los bytes individualmente
    data = bytearray(f.read())

# 1. Reparar el Offset donde empiezan los píxeles (Byte 10)
# Queremos poner 54 (0x36 en hex)
data[10] = 0x36
data[11] = 0x00
data[12] = 0x00
data[13] = 0x00

# 2. Reparar el tamaño de la cabecera DIB (Byte 14)
# Queremos poner 40 (0x28 en hex)
data[14] = 0x28
data[15] = 0x00
data[16] = 0x00
data[17] = 0x00

# Guardamos el resultado en un nuevo archivo BMP
with open("tunn3l_v1s10n_reparado.bmp", "wb") as f:
    f.write(data)

print("¡Cabeceras reparadas! Archivo guardado como tunn3l_v1s10n_reparado.bmp")


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ explorer.exe tunn3l_v1s10n_reparado.bmp

```
![[Pasted image 20261005130005.png]]
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ nano redimencion.py
# Abrimos la imagen que ya tiene las cabeceras principales reparadas
with open("tunn3l_v1s10n_reparado.bmp", "rb") as f:
    data = bytearray(f.read())

# El alto de la imagen empieza en el byte 22.
# Vamos a cambiarlo a 850 píxeles (0x0352 en hexadecimal).
# Recordando usar Little Endian:
data[22] = 0x52
data[23] = 0x03
data[24] = 0x00
data[25] = 0x00

# Guardamos la imagen final
with open("tunn3l_v1s10n_final.bmp", "wb") as f:
    f.write(data)

print("¡Altura modificada! Abre tunn3l_v1s10n_final.bmp")



completamos la bandera con academy y 20}

```

![[Pasted image 20261005130128.png]]

```
academy{qu1t3_a_v13w_2020}
```

## notas adicionales

## referencias
