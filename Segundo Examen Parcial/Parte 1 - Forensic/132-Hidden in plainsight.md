## Descripción
You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. Your task is to discover the hidden payload and extract the flag. Download the jpg image [here](https://challenge-files.cylabacademy.net/library/9ec77a1b83f3b582954d97ec39f7926d4dc45f98cd1ef7a24b3172ca385e02b2/img.jpg).

Download the jpg image and read its metadata
## solución 
1. Descargar la imagen
2. Usar exiftool img.jpg
3. Al ver en los datos observamos que existe el comentario cifrado en base 64 asi que lo decodificamos con: echo "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9" | base64 -d El resultado es steghide:cEF6endvcmQ= que nos indica el lugar y la contraseña para acceder a el.
4. Utilizamos steghide extract -sf img.jpg y cuando se nos pida la contraseña la ingresamos.
5. Utilizamos lo siguiente para obtener la bandera.

```

echo "cEF6endvcmQ=" | base64 -d # -> pAzzword 
steghide extract -sf img.jpg -p pAzzword 
cat flag.txt


pAzzword
```

```
academy{h1dd3n_1n_1m4g3_71ae1957}
```
## notas adicionales

## referencias
[From Base64 - CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=Y0VGNmVuZHZjbVE9)