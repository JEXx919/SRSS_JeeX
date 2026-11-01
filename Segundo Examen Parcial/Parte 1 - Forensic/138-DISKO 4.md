## Descripción
Can you find the flag in this disk image? This time I deleted the file! Let see you get it now! Download the disk image [here](https://challenge-files.cylabacademy.net/library/73410159cc8aafa59ec856dcc13ab8b30a50f6827eef6627d3e346bbd3c0085a/disko-4.dd.gz).

How would you look for deleted files?
## solución
1. Se descargó y descomprimió la imagen de disco:
    
    ```shell
    gzip -d disko-4.dd.gz
    ```
    
2. Se buscaron los archivos eliminados utilizando `fls`:
    
    ```shell
    fls -r disko-4.dd | grep "\*"
    ```
    
    Se encontraron los siguientes archivos:
    
    ```
    + r/r * 522629: messages
    + r/r * 532021: dont-delete.gz
    ```
    
3. Se recuperó el archivo `dont-delete.gz` mediante su número de inodo `532021`:
    
    ```shell
    icat disko-4.dd 532021 > dont-delete.gz
    ```
    
4. Se descomprimió y visualizó el contenido del archivo recuperado:
    
    ```shell
    gzip -dc dont-delete.gz
    ```
    
    Se obtuvo el siguiente resultado:
    

```
academy{d3l_d0n7_h1d3_w3ll_9748d144}
```
## notas adicionales

## referencias
