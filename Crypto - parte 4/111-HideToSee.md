## Descripción
How about some hide and seek heh? Look at this image [here](https://challenge-files.cylabacademy.net/library/4430e164c62a6474394efb666c3b2c24511a0823a3408e5e7a19a37940f0e592/atbash.jpg).

Download the image and try to extract it.
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ steghide extract -sf atbash.jpg
Enter passphrase:
wrote extracted data to "encrypted.txt".

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat encrypted.txt
zxzwvnb{zgyzhs_xizxp_6167yw8v}

atbash cipher

academy{atbash_crack_6167bd8e}

```

```
academy{atbash_crack_6167bd8e}
```
## notas adicionales

## referencias
[Atbash Cipher - CyberChef](https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher\(\)&input=enh6d3ZuYnt6Z3l6aHNfeGl6eHBfNjE2N3l3OHZ9)