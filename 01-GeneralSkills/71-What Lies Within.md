## Descripcion

## solucion 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ strings buildings.png
no resultados

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ xxd buildings.png 

no resultados...


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ explorer.txt buildings.png



nos vamos a la pajina web 
https://stylesuxx.github.io/steganography/
subimos el archivo en decodeficiar y obtenemos 
academy{h1d1ng_1n_th3_b1t5}


metodo # 2


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ zsteg -a buildings.png
b1,rgb,lsb,xy       .. text: "academy{h1d1ng_1n_th3_b1t5}"


```

```
academy{h1d1ng_1n_th3_b1t5}
```
## notas adicionales

## referencias
[Esteganografía en línea](https://stylesuxx.github.io/steganography/)