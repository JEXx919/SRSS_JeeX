## Descripción
Can you figure out how this program works to get the flag? Connect to the program with netcat:

`$ nc chatelaine.cylabacademy.net 18400`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/8fffd28e5e71954eff5b80565e7f04fb0abfb5e57c7f218bc00474bf9d9ecc10/picker-IV.c). The binary can be downloaded [here](https://challenge-files.cylabacademy.net/library/8fffd28e5e71954eff5b80565e7f04fb0abfb5e57c7f218bc00474bf9d9ecc10/picker-IV).

With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.

How can you find the address that `win` is at?
## solución 
```
descargar los archivos y buscar..

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ nm picker-IV | grep win
00000000004012a1 T win

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ nc chatelaine.cylabacademy.net 33602
Enter the address in hex to jump to, excluding '0x': 4012a1
You input 0x4012a1
You won!
academy{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_f0fec8d0}



```

```
academy{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_f0fec8d0}
```
## notas adicionales

## referencias
