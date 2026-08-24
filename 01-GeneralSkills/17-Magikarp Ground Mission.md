## Descripcion
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.
Finding a cheatsheet for bash would be really helpful!
## solucion 
```
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_

2da parte 
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat instructions-to-2of3.txt
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  challenge  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt
0ut_0f_//4t3r_
ctf-player@pico-chall$ 



3er parte 
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  challenge  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat instructions-to-3of3.txt
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt
0b24fc4f}

```

```
picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}

```
## notas adicionales
accedemos al servidor con los datos que nos indican y dentro de este tendremos directorios y instrucciones siguiendo dichas instrucciones navegaremos por los directorios hasta encontrar todas las partes de la bandera.
## referencias
[Webshell](https://webshell.cylabacademy.org/)