## Descripción
Can you decrypt this message? Decrypt this [message](https://challenge-files.cylabacademy.net/library/7e1288d31bc6645f95d07bcf09caaf93210591ba082ba0f14490f0767ad7fd33/cipher.txt) using this key "CYLAB".

[https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher)
## solución 
```

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/7e1288d31bc6645f95d07bcf09caaf93210591ba082ba0f14490f0767ad7fd33/cipher.txt
--2026-10-25 00:01:24--  https://challenge-files.cylabacademy.net/library/7e1288d31bc6645f95d07bcf09caaf93210591ba082ba0f14490f0767ad7fd33/cipher.txt
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.37, 13.226.187.40, 13.226.187.66, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.37|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43 [application/octet-stream]
Saving to: ‘cipher.txt’

cipher.txt                    100%[=================================================>]      43  --.-KB/s    in 0s

2026-10-25 00:01:25 (16.0 MB/s) - ‘cipher.txt’ saved [43/43]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat cipher.txt
caldfow{O0NU_WQ3_G1G3O3T3_A1AH3S_4c372077}


academy{D0NT_US3_V1G3N3R3_C1PH3R_4a372077}



```

```
academy{D0NT_US3_V1G3N3R3_C1PH3R_4a372077}
```
## notas adicionales

## referencias
[Cifrado de Vigenere - Descifrar con o sin Clave - Decodificador Online](https://www.dcode.fr/cifrado-vigenere)