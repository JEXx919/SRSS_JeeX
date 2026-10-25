## Descripción
A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? Download the message [here](https://challenge-files.cylabacademy.net/library/54f070d7a4fbb401b7ae06e5f41a3071cc195039368a58d9c6bb6f5a95b7913c/message.txt).

The decoded message names a phrase. Put that phrase, and nothing else, in the academy flag format: `academy{phrase}`.

Once you've understood how the cipher works, it's best to draw it out yourself on paper
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat message.txt
Ta _7N6D86hlg:W3D_H3C31N__C16ef sHR053F38N43DE1 i33___NF


script

mensaje = "Ta _7N6D86hlg:W3D_H3C31N__C16ef sHR053F38N43DE1 i33___NF"

rieles = 4
longitud = len(mensaje)

# Registrar en qué riel va cada carácter
patron = []
riel = 0
direccion = 1

for posicion in range(longitud):
    patron.append(riel)

    if riel == 0:
        direccion = 1
    elif riel == rieles - 1:
        direccion = -1

    riel += direccion

# Contar los caracteres de cada riel
cantidades = [patron.count(numero) for numero in range(rieles)]

# Distribuir el texto cifrado entre los rieles
filas = []
inicio = 0

for cantidad in cantidades:
    filas.append(list(mensaje[inicio:inicio + cantidad]))
    inicio += cantidad

# Leer los rieles siguiendo el zigzag original
indices = [0] * rieles
resultado = ""

for riel in patron:
    resultado += filas[riel][indices[riel]]
    indices[riel] += 1

print(resultado)




WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_8CEF1166




```

```
academy{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_8CEF1166}
```
## notas adicionales

## referencias
