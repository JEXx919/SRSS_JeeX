## Descripción
Can you get the real meaning from this file.

Download the file [here](https://challenge-files.cylabacademy.net/library/0d5754d51dc425dbb46c76eef33bb2b596a1a3bc6f4163ddd2a215f7e0d45198/enc_flag).

Engaging in various decoding processes is of utmost importance

## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget https://challenge-files.cylabacademy.net/library/0d5754d51dc425dbb46c76eef33bb2b596a1a3bc6f4163ddd2a215f7e0d45198/enc_flag
--2026-10-12 22:56:13--  https://challenge-files.cylabacademy.net/library/0d5754d51dc425dbb46c76eef33bb2b596a1a3bc6f4163ddd2a215f7e0d45198/enc_flag
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.22, 13.226.187.66, 13.226.187.37, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag                               100%[==========================================================================>]      73  --.-KB/s    in 0s

2026-10-12 22:56:13 (960 KB/s) - ‘enc_flag’ saved [73/73]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ file enc_flag
enc_flag: ASCII text

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat enc_flag
YidhR3BvYTJ4MFpudHFhR3g2YUhsZmF6TnFlVGwzWVROclh6Z3hiR3M1YlRBeWZRPT0nCg==

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat enc_flag | base64 -d
b'aGpoa2x0ZntqaGx6aHlfazNqeTl3YTNrXzgxbGs5bTAyfQ=='


b'aGpoa2x0ZntqaGx6aHlfazNqeTl3YTNrXzgxbGs5bTAyfQ=='

aGpoa2x0ZntqaGx6aHlfazNqeTl3YTNrXzgxbGs5bTAyfQ==

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ echo aGpoa2x0ZntqaGx6aHlfazNqeTl3YTNrXzgxbGs5bTAyfQ== | base64 -d
hjhkltf{jhlzhy_k3jy9wa3k_81lk9m02}


ROT13 19 rotaciones
academy{caesar_d3cr9pt3d_81ed9f02}

```

```
academy{caesar_d3cr9pt3d_81ed9f02}
```
## notas adicionales

## referencias
[ROT13 - CyberChef](https://gchq.github.io/CyberChef/#recipe=ROT13\(true,true,false,19\)&input=aGpoa2x0ZntqaGx6aHlfazNqeTl3YTNrXzgxbGs5bTAyfQ)
