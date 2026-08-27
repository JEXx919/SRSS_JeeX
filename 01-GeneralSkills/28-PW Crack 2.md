## Descripcion
Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py
--2026-08-27 05:27:20--  https://artifacts.picoctf.net/c/15/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.95, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                       100%[=====================================================================================================>]     914  --.-KB/s    in 0s      

2026-08-27 05:27:20 (748 MB/s) - 'level2.py' saved [914/914]

JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
--2026-08-27 05:27:31--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                             100%[=====================================================================================================>]      31  --.-KB/s    in 0s      

2026-08-27 05:27:31 (12.6 MB/s) - 'level2.flag.txt.enc' saved [31/31]

JeeX7ZaZ-academy@webshell:~$ 
JeeX7ZaZ-academy@webshell:~$ nano level2.py
JeeX7ZaZ-academy@webshell:~$ python3 level2.py
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}

codigo python
  GNU nano 6.2                                                                               level2.py                                                                                        
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

flag_enc = open('level2.flag.txt.enc', 'rb').read()



def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_2_pw_check()


```

```
picoCTF{tr45h_51ng1ng_502ec42e}
```
## notas adicionales
descargue ambos archivos y al visualizar el .py con nano me percate que la contrasela estaba en hexadecimal asi que solo la convertí.
## referencias
