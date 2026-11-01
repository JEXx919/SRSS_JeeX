## Descripción
This file doesn't look like much... just a bunch of 1s and 0s. But maybe it's not just random noise. Can you recover anything meaningful from this? Download the file [here](https://challenge-files.cylabacademy.net/library/819e05da202722f7847eab5c0efdedc194be8a2bc19e6b436d057c8514ae70bc/digits.bin).
## solución 
1. Se descargó el archivo `digits.bin` y se analizó su formato mediante el comando: `file digits.bin` El resultado indicó que se trataba de un archivo de texto ASCII.
    
2. Se visualizaron los primeros caracteres mediante: `head -c 100 digits.bin` Se comprobó que el archivo contenía una secuencia de ceros y unos.
    
3. Se creó un script en Python utilizando el editor de texto Nano: `nano decode.py`
    
4. Dentro del archivo se escribió el siguiente código para convertir los bits en bytes:
```
with open("digits.bin", "r") as archivo:
    bits = archivo.read().strip()

datos = bytes(
    int(bits[i:i+8], 2)
    for i in range(0, len(bits), 8)
    if len(bits[i:i+8]) == 8
)

with open("decoded.bin", "wb") as archivo:
    archivo.write(datos)

print("Archivo decodificado: decoded.bin")
print("Primeros bytes:", datos[:20].hex())
```
1. Se ejecutó el programa utilizando: `python3 decode.py` El script generó un nuevo archivo llamado `decoded.bin`.
    
2. Se identificó el formato del archivo generado mediante: `file decoded.bin` El resultado mostró que se trataba de una imagen JPEG de 800 × 500 píxeles.
    
3. Se cambió el nombre del archivo y se abrió la imagen mediante los comandos:

```shell
    mv decoded.bin imagen.jpg
    xdg-open imagen.jpg
```
. Finalmente, se visualizó la imagen reconstruida y se identificó la bandera escrita en su interior.


```
academy{h1dd3n_1n_th3_b1n4ry_5a7375c5}
```
## notas adicionales

## referencias
