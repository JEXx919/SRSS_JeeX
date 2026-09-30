## Descripcion
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.cylabacademy.net/library/53f38374e47a48424dc7e9100aba4e4b42a590f3921cfc31188171ae7d6d61e3/whitepages.txt) is all blank!

  
There is data encoded somewhere... there might be an online decoder.
## solucion 
```


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ xxd whitepages.txt
00000000: e280 83e2 8083 e280 83e2 8083 20e2 8083  ............ ...
00000010: 20e2 8083 e280 8320 20e2 8083 e280 83e2   ......  .......
00000020: 8083 e280 8320 e280 8320 20e2 8083 e280  ..... ...  .....
00000030: 83e2 8083 2020 e280 8320 20e2 8083 e280  ....  ...  .....
00000040: 83e2 8083 e280 8320 e280 8320 20e2 8083  ....... ...  ...
00000050: e280 8320 e280 83e2 8083 e280 8320 20e2  ... .........  .
00000060: 8083 e280 8320 e280 8320 e280 8320 20e2  ..... ... ...  .
00000070: 8083 2020 e280 8320 e280 8320 2020 20e2  ..  ... ...    .

# Abre el archivo en modo lectura binaria
with open("whitepages.txt", "rb") as f:
    data = f.read()

# Reemplazamos el espacio especial (Em space) por '0'
# y el espacio normal por '1'
data = data.replace(b'\xe2\x80\x83', b'0')
data = data.replace(b'\x20', b'1')

# Convertimos los bytes restantes a texto
binary_str = data.decode('ascii')

# Agrupamos los 0s y 1s en bloques de 8 bits para convertirlos a caracteres ASCII
flag = ""
for i in range(0, len(binary_str), 8):
    byte = binary_str[i:i+8]
    if len(byte) == 8:
        # Convierte el byte (ej: '01110000') a entero base 2, y luego a su carácter
        flag += chr(int(byte, 2))

print(flag)





┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python res.py

academy

SEE PUBLIC RECORDS & BACKGROUND REPORT
5000 Forbes Ave, Pittsburgh, PA 15213
academy{not_all_spaces_are_created_equal_19fc1787ee14ef2c56ee0cddc142a0d9}

```

```
academy{not_all_spaces_are_created_equal_19fc1787ee14ef2c56ee0cddc142a0d9}
```
## notas adicionales

## referencias
