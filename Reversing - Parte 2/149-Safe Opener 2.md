## Descripción
What can you do with this file? I forgot the key to my safe but this [file](https://challenge-files.cylabacademy.net/library/867399a60e44754a85257c7eb1afa26731c73afa90daafcd4779710c9fa4a05e/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

Download and try to decompile the file.
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget "https://challenge-files.cylabacademy.net/library/867399a60e44754a85257c7eb1afa26731c73afa90daafcd4779710c9fa4a05e/SafeOpener.class"
--2026-11-07 22:06:04--  https://challenge-files.cylabacademy.net/library/867399a60e44754a85257c7eb1afa26731c73afa90daafcd4779710c9fa4a05e/SafeOpener.class
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.37, 13.226.187.66, 13.226.187.22, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.37|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2036 (2.0K) [application/octet-stream]
Saving to: ‘SafeOpener.class’

SafeOpener.class              100%[=================================================>]   1.99K  --.-KB/s    in 0s

2026-11-07 22:06:04 (30.2 MB/s) - ‘SafeOpener.class’ saved [2036/2036]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ strings SafeOpener.class | grep -i academy
,academy{SAf3_0p3n3rr_y0u_solv3d_it_87a1d928}
```

```
academy{SAf3_0p3n3rr_y0u_solv3d_it_87a1d928}
```
## notas adicionales

## referencias
