## Descripción
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.cylabacademy.net/library/fa43fd31bc6abcac3fa8a68795def44e6ee31e3c4caf0bd11810a545141bf0dd/scrambled1.png) [scrambled2.png](https://challenge-files.cylabacademy.net/library/fa43fd31bc6abcac3fa8a68795def44e6ee31e3c4caf0bd11810a545141bf0dd/scrambled2.png)

[https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)

Think of different ways you can "stack" images
## solución 
![[Pasted image 20261021125052.png]]
```
Descargar las 2 imagenes

script de python

img1 = Image.open("scrambled1.png")
img2 = Image.open("scrambled2.png")

arr1 = np.array(img1)
arr2 = np.array(img2)

(módulo 256),

mezcla = arr1 + arr2

resultado = Image.fromarray(mezcla)


resultado.show()
resultado.save("flag_revelada.png")



Sobreponerlas y aparece la flag


academy{2f16d0c4}
```

```
academy{2f16d0c4}
```
## notas adicionales

## referencias
