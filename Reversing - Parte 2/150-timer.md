## Descripción
You will find the flag after analysing this apk Download [here](https://challenge-files.cylabacademy.net/library/b31248aec6287cbe220d0dbfa55e216b87e6175b3561d441062bfdd018f3cacc/timer.apk).

Decompile

mobsf or jadx
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ jadx -d ~/timer_decomp ~/timer.apk
INFO  - loading ...
INFO  - processing ...
ERROR - finished with errors, count: 3

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ grep -Rni "academy" ~/timer_decomp/
/home/jeex/timer_decomp/resources/AndroidManifest.xml:4:    android:versionName="academy{t1m3r_r3v3rs3d_succ355fully_17496}"
/home/jeex/timer_decomp/sources/com/example/timer/BuildConfig.java:9:    public static final String VERSION_NAME = "academy{t1m3r_r3v3rs3d_succ355fully_17496}";
/home/jeex/timer_decomp/sources/androidx/core/util/PatternsCompat.java:15:    static final String IANA_TOP_LEVEL_DOMAINS = "(?:(?:aaa|aarp|abb|abbott|abogado|academy|accenture|accountant|accountants|aco|active|actor|ads|adult|aeg|aero|afl|agency|aig|airforce|airtel|allfinanz|alsace|amica|amsterdam|android|apartments|app|apple|aquarelle|aramco|archi|army|arpa|arte|asia|associates|attorney|auction|audio|auto|autos
```

```
academy{t1m3r_r3v3rs3d_succ355fully_17496}
```
## notas adicionales

## referencias
