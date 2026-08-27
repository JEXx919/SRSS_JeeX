## Descripcion

## solucion 
```
JeeX7ZaZ-academy@webshell:~$ rm -rf *
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.py
--2026-08-27 05:21:54--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.40, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                       100%[=====================================================================================================>]     876  --.-KB/s    in 0s      

2026-08-27 05:21:54 (471 MB/s) - 'level1.py' saved [876/876]

JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
--2026-08-27 05:22:09--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.95, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                             100%[=====================================================================================================>]      30  --.-KB/s    in 0s      

2026-08-27 05:22:09 (15.0 MB/s) - 'level1.flag.txt.enc' saved [30/30]

JeeX7ZaZ-academy@webshell:~$ nano level1.py
JeeX7ZaZ-academy@webshell:~$ python3 level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
JeeX7ZaZ-academy@webshell:~$ 




codigo de python
  GNU nano 6.2                                                                               level1.py                                                                                        
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()

```

```
picoCTF{545h_r1ng1ng_1b2fd683}
```
## notas adicionales
jjajajsj observamos el código y en el mismo se encuentra la contraseña
## referencias
