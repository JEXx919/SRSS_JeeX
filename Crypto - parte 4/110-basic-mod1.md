## Descripción

We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://challenge-files.cylabacademy.net/library/23b095a85da350dcda44aefdf5a62785a023f5d4570374d08eef71aefd096f7f/message.txt).

Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.

Wrap your decrypted message in the academy flag format (i.e. `academy{decrypted_message}`)

Do you know what `mod 37` means?

`mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.
## solución 
```

scrit de python
  GNU nano 9.0                                             xdc.py
arch = open('message.txt').read().split()

flag = ''

for c in arch:
        n = int(c)
        m = n % 37
        if m >= 0 and m <= 25:
                l =  chr(m + 65)
        elif m>=26 and  m<=35:
                l = chr(m + 22)
        else:
                l = '_'

        flag += l

        print(f'{c} - {m} - {l}')

print('academy{'+flag+'}')


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python3 xdc.py
91 - 17 - R
396 - 26 - 0
316 - 20 - U
198 - 13 - N
225 - 3 - D
369 - 36 - _
50 - 13 - N
369 - 36 - _
350 - 17 - R
63 - 26 - 0
205 - 20 - U
346 - 13 - N
299 - 3 - D
406 - 36 - _
330 - 34 - 8
397 - 27 - 1
335 - 2 - C
374 - 4 - E
71 - 34 - 8
111 - 0 - A
179 - 31 - 5
64 - 27 - 1
academy{R0UND_N_R0UND_81CE8A51}

```

```
academy{R0UND_N_R0UND_81CE8A51}
```
## notas adicionales

## referencias
