## Descripcion
Decode this [message](https://challenge-files.cylabacademy.net/library/d825fde6581b1311eafdd403da1cc96f1f98fe3fe84cd71d850310ebb3908088/message.wav) from the moon.

How did pictures from the moon landing get sent back to Earth?
  
What is the CMU mascot?, that might help select a RX option
## solucion 
```
clonar repositorio y instalar...
# 1. Instalar la dependencia que faltaba (por si acaso)
sudo apt install python3-setuptools

# 2. Descargar el decodificador
git clone https://github.com/colaclanth/sstv.git

# 3. Entrar a la carpeta descargada
cd sstv

# 4. Instalar la herramienta correctamente
sudo python3 setup.py install

# 5. Regresar a tu carpeta principal (donde está tu message.wav)
cd ~

# 6. Ejecutar la decodificación del audio a imagen
sstv -d message.wav -o bandera.png


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ sstv -d message.wav -o bandera.png
[sstv] Searching for calibration header... Found!
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...                                   [####################################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!

```
![[Pasted image 20260930133641.png]]
```
picoCTF{beep_boop_im_in_space}
```
## notas adicionales

## referencias
