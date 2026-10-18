## Descripción
Now you DON’T see me. This [report](https://challenge-files.cylabacademy.net/library/455e6e9581a9272cf0cd6a8f2da0a7cdcfefdb52dc7a7f9c09a27705e2c94103/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

How can you be sure of the redaction?
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/455e6e9581a9272cf0cd6a8f2da0a7cdcfefdb52dc7a7f9c09a27705e2c94103/Financial_Report_for_ABC_Labs.pdf
--2026-10-17 23:10:44--  https://challenge-files.cylabacademy.net/library/455e6e9581a9272cf0cd6a8f2da0a7cdcfefdb52dc7a7f9c09a27705e2c94103/Financial_Report_for_ABC_Labs.pdf
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.22, 13.226.187.40, 13.226.187.37, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1817 (1.8K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Report_for_ABC_Labs 100%[=================================================>]   1.77K  --.-KB/s    in 0s

2026-10-17 23:10:45 (19.8 MB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [1817/1817]

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ pdftotext -layout Financial_Report_for_ABC_Labs.pdf -
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.

Breakdown - Just painted over in MS word.



Cost Benefit Analysis

Credit             Debit



This is not the flag, keep looking



Expenses from the

academy{C4n_Y0u_S33_m3_fully}



Redacted document.

```

```
academy{C4n_Y0u_S33_m3_fully}
```
## notas adicionales

## referencias
