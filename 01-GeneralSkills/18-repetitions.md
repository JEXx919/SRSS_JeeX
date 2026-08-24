## Descripcion

Can you make sense of this file?

Download the file [here](https://artifacts.picoctf.net/c/474/enc_flag).

  
Multiple decoding is always good.

## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/474/enc_flag
--2026-08-24 19:44:19--  https://artifacts.picoctf.net/c/474/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag                                        100%[=====================================================================================================>]     349  --.-KB/s    in 0s      

2026-08-24 19:44:19 (131 MB/s) - 'enc_flag' saved [349/349]

JeeX7ZaZ-academy@webshell:~$ ls
enc_flag
JeeX7ZaZ-academy@webshell:~$ file enc_flag
enc_flag: ASCII text
JeeX7ZaZ-academy@webshell:~$ cat enc_flag
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZhTTBKUFdXdGtlbVF4V2tkWGJYUllDbUY2UWpSWmEyaFRWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
```

```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_3f81f7be}
```
## notas adicionales
base 64 anidados, usando cybercheff anide 6 conversores de base 64
al texto del archivo y asi obtuve la respuesta.
## referencias
[From Base64, 5 more - CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)From_Base64\('A-Za-z0-9%2B/%3D',true,false\)From_Base64\('A-Za-z0-9%2B/%3D',true,false\)From_Base64\('A-Za-z0-9%2B/%3D',true,false\)From_Base64\('A-Za-z0-9%2B/%3D',true,false\)From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=Vm1wR1UxRXlSWGxVV0d4VFlteEtWVll3WkZOV2JHeHlWMjFHVjFKdGVEQlViRnBQWVd4S2RGVnNhRnBXVmxVeFdWWmFTMVpXV25WaA0KUm1SWFpXdGFiMWRXV210U01rNXlUbFpXV0FwaVZWcFVWbTEwZDFWV1pGZFZhMlJwWWxaYVdGWnROVmRWWjNCcFUwVktlbGRXVWtOaw0KTWxaWFZsaG9XR0pZUWs5VmJGSlhVMFprY1ZSdVRsZGFNMEpaVldwR1MyVldXa2RhU0dSWENrMXNXbnBXVjNoaFZtMUtSazVYT1ZWVw0KVmtwRVZHeGFZVmRGTVZoU2JGWmhUVEJLVUZkWGRHdGxiVkY0VjJ0a1dHSllVbGxEYlVZMlVXcFNXbUV5YUZSV2FrcEhaRWRXUmxacw0KYUdrS1lsUnJlbFpFUmxkVU1rcHpVV3hXVGxKWVRreERaejA5Q2c9PQ&ieol=CRLF)