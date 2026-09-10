## Descripcion
Find the flag being held on this server to get ahead of the competition

http://wily-courier.picoctf.net:52667/

Maybe you have more than 2 choices
Check out tools like Burpsuite to modify your requests and look at the responses
## solucion 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ curl -s -I http://wily-courier.picoctf.net:52667/
HTTP/1.1 200 OK
Date: Mon, 07 Sep 2026 16:34:40 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8


```

```
picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
```
## notas adicionales
curl
## referencias
