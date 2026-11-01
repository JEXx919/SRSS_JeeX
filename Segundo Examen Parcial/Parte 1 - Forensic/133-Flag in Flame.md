## Descripción
The SOC team discovered a suspiciously large log file after a recent breach. When they opened it, they found an enormous block of encoded text instead of typical logs. Could there be something hidden within? Your mission is to inspect the resulting file and reveal the real purpose of it. The team is relying on your skills to uncover any concealed information within this unusual log. Download the encoded data here: [Logs Data](https://challenge-files.cylabacademy.net/library/8389f7eb8ae95fd4453f1e2d27498905b415efec5fc738bfd0983d56c09959bf/logs.txt). Be prepared—the file is large, and examining it thoroughly is crucial .

Use `base64` to decode the data and generate the image file.
## solución 
```
**1. El log es una imagen en Base64.** Al decodificarlo sale un PNG de 896×1152 con la ilustración de un hacker: correr:


base64 -d logs.txt > imagen.png
file imagen.png 


**2. La imagen tiene una línea de texto en hexadecimal** en la parte de abajo, sobre el escritorio:


61636164656D797B666F72656E736963735F616E616C797369735F69735F616D617A696E675F64666332623462397D

 echo "61636164656D797B666F72656E736963735F616E616C797369735F69735F616D617A696E675F64666332623462397D" | xxd -r -p 
 
 
```


```
academy{forensics_analysis_is_amazing_dfc2b4b9}
```

## notas adicionales

## referencias
