## Descripción
Can you find the flag in this disk image? Wrap what you find in the academy{} flag format. Download the disk image [here](https://challenge-files.cylabacademy.net/library/0b369ed5974a5e777ca3bc323bd39d75a6f27762a449d16cd2a0ffc08b2a6aa8/timeline-1-partition4.img.gz).

Create a Sleuthkit MAC timeline!

Look at recent timestamps

Pay close attention to timestamps near an anti-forensic action

Filter only new files by grepping for `macb`
## solución 
1. Se descomprimió la imagen de disco y se renombró:
    
    ```shell
    gzip -d timeline-1-partition4.img.gz
    mv timeline-1-partition4.img timeline1.img
    ```
    
2. Se generó una línea de tiempo mediante The Sleuth Kit:
    
    ```shell
    fls -r -m / timeline1.img > body.txt
    mactime -b body.txt -d > mactime.csv
    ```
    
3. Se filtraron los archivos con marcas temporales `macb` para identificar actividad reciente:
    
    ```shell
    grep "macb" mactime.csv | tail -n 10
    ```
    
    Se identificó el archivo `/etc/chat`, creado el 1 de diciembre de 2025, con inodo `32716`.
    
4. Se extrajo el contenido del archivo utilizando su inodo:
    
    ```shell
    icat timeline1.img 32716
    ```
    
    Se obtuvo la siguiente cadena codificada:
    
    ```
    NTczNDE3aDEzcl83aDRuXzdoM18xNDU3XzU4NTI3YmIyMjIK
    ```
    
5. Se decodificó la cadena mediante Base64:
    
    ```shell
    echo "NTczNDE3aDEzcl83aDRuXzdoM18xNDU3XzU4NTI3YmIyMjIK" | base64 -d
    ```
    
    Se recuperó el mensaje utilizado para construir la bandera.
    

```
academy{573417h13r_7h4n_7h3_1457_58527bb222}
```
## notas adicionales

## referencias
