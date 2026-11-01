## Descripción
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://challenge-files.cylabacademy.net/library/764d21f0248d7c1df55583eb1ad863dad241f86f90dd2717e8aa5b9fc3a7e26e/anthem.flag.txt)

1. Download the file and search for the flag based on the known prefix.

## solución 
```
Para encontrar la bandera en el archivo que descargaste, debes usar el comando `grep` apuntando directamente a `anthem.flag.txt`.

**Paso 1: Abrir la terminal** Abre tu terminal y navega hasta la carpeta exacta donde guardaste el archivo `anthem.flag.txt`.

**Paso 2: Ejecutar la búsqueda** Como el archivo es un texto extenso, utiliza `grep` para filtrar únicamente la línea que contiene el prefijo de la bandera. Ejecuta este comando exacto:

grep "academy{" anthem.flag.txt

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ grep "academy{" anthem.flag.txt
      we think that the men of academy{gr3p_15_@w3s0m3_33595e98}
```

```
academy{gr3p_15_@w3s0m3_33595e98}
```
## notas adicionales

## referencias
