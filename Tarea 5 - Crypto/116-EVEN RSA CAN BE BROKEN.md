## Descripción
This service provides you an encrypted flag. Can you decrypt it with just N & e? Connect to the program with netcat:

`$ nc xebec.cylabacademy.net 33372`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/548e8da21a43607b2b9c2bf9c7c374828e84cfd56fb38a24958eb8963afa09f1/encrypt.py).

How much do we trust randomness?
Notice anything interesting about N?
Try comparing N across multiple requests
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ nc xebec.cylabacademy.net 13799
N: 24499850756121398482397909867493357595642307528950947405254479594627364980689757910148854726132075120848496940495782916192213319273293455972579665658383826
e: 65537
cyphertext: 5976848136155490203132251396430201213623763651776794947295412717656186828978668413592899396845074190429616374805098503222015593824778189091173638028514451

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python
Python 3.14.7 (main, Sep  5 2026, 05:55:41) [GCC 16.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> n = 244998507561213984823979098674933575956423075289509474052544795946273649806897579101488547261320751208484969404\
95782916192213319273293455972579665658383826
>>> e = 65537
>>> c = 597684813615549020313225139643020121362376365177679494729541271765618682897866841359289939684507419042961637480\
5098503222015593824778189091173638028514451

>>> n % 2
0
>>> p = 2
>>> q = n // 2
>>> tn = (p - 1) * (q - 1)
>>> d = pow(e, -1, tn)
>>> m = pow(c, d, n)
>>> bytes.fromhex( hex(m)[2:] ).decode()
'academy{tw0_1$_pr!m3207f407f}'
```

```
academy{tw0_1$_pr!m3207f407f}
```
## notas adicionales

## referencias
