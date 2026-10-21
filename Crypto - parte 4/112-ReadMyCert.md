## Descripción
How about we take you on an adventure on exploring certificate signing requests Take a look at this CSR file [here](https://challenge-files.cylabacademy.net/library/936e82e74aef68c1a8fcc80b032ea33d65adda1f04b5c46085d44a5d6ff7cb71/readmycert.csr).

Download the certificate signing request and try to read it.
## solución 
```

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/936e82e74aef68c1a8fcc80b032ea33d65adda1f04b5c46085d44a5d6ff7cb71/readmycert.csr
--2026-10-21 11:25:11--  https://challenge-files.cylabacademy.net/library/936e82e74aef68c1a8fcc80b032ea33d65adda1f04b5c46085d44a5d6ff7cb71/readmycert.csr
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.37, 13.226.187.66, 13.226.187.40, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.37|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 997 [application/octet-stream]
Saving to: ‘readmycert.csr’

readmycert.csr                100%[=================================================>]     997  --.-KB/s    in 0s

2026-10-21 11:25:12 (19.2 MB/s) - ‘readmycert.csr’ saved [997/997]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat readmycert.csr
-----BEGIN CERTIFICATE REQUEST-----
MIICpzCCAY8CAQAwPDEmMCQGA1UEAwwdYWNhZGVteXtyZWFkX215Y2VydF9kY2Zi
OWM3Nn0xEjAQBgNVBCkMCWN0ZlBsYXllcjCCASIwDQYJKoZIhvcNAQEBBQADggEP
ADCCAQoCggEBAJCOkw4jpZdcu3XvYdZqT2UT3m0BIdxUD7gluZacs72NudXTxM9i
MXO/HKRm4XSKbTXvpq9C2x6M2uMK0BzQP8AfNRuZdjFm7+gP/lhCpswbD+XIn1G6
KvrMgRshba0pIM/xvn4RerMiZt992NfEBwSxt+V3mm8QovC0JHpjt0gQCagVgJsg
XVp4zmtQWqMxZZytDenOFU2zg9U4fhwWBtWELCtDGZi+wY7WphdHNEcbEJfqVOmy
ZxhXbPbMawo+JpGJaysWyn1vUW9SClgR1QdIN8/8LRy6GARx8a8G6STzwn64KZHs
bpkuT8uvv9qIAl2ISvMiRThPffpqHGiGPj0CAwEAAaAmMCQGCSqGSIb3DQEJDjEX
MBUwEwYDVR0lBAwwCgYIKwYBBQUHAwIwDQYJKoZIhvcNAQELBQADggEBACEVvFvQ
ZJwf7HWDf0EMJ1HQUSm6soMkGNc/CO+Zw04adfk9cMmKbAc7PR0yFG3DlBjesJd8
U9T82FGCWNoekz1Mhf5FjDpJykDIEdiPIHDBDdmuFN66oO3r6BAR4PkcUO29v+OO
jWLG/UhrNaGP3E7Jny3RJTFgTwolsy7++RL37l2O/hfwMlMZPE3s5f++3ilLUM/3
Jc7+9lqzk3sBAp/Q9dSPeWHLycJi8sqZn58ENznKB1nD/OloydOO9uJ1txFhbMGZ
Nw5r/1RmEK7vneffPbn6EFcyKr0+6st5aixNVinGMVKouxh+aAPV+Hj66LjgqBGk
xweoSX2m7o9k62Y=
-----END CERTIFICATE REQUEST-----


openssl req -in readmycert.csr -noout -text


```

```
academy{read_mycert_dcfb9c76}
```
## notas adicionales

## referencias
