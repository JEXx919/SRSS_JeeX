## Descripcion
Find the flag in the Python script!
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c/35/serpentine.py
--2026-08-27 05:42:30--  https://artifacts.picoctf.net/c/35/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.64, 3.160.5.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: 'serpentine.py'

serpentine.py                                   100%[=====================================================================================================>]   2.49K  --.-KB/s    in 0s      

2026-08-27 05:42:30 (1.03 GB/s) - 'serpentine.py' saved [2550/2550]

JeeX7ZaZ-academy@webshell:~$ nano -l serpentine.py 
JeeX7ZaZ-academy@webshell:~$ python3 serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) a

-----------------------------------------------------
Look how far you've come!
-----------------------------------------------------


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
JeeX7ZaZ-academy@webshell:~$ 

solucion
JeeX7ZaZ-academy@webshell:~$ python3 serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Porsupuesto aqui tienes!!!!!!!


picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) 








codigo python corregido
solo hacer que la opccion b 
llamara a la funcion de imprimir bandera
elif choice == 'b':
69       print('\nPorsupuesto aqui tienes!!!!!!!\n\n')
70       print_flag()
```

```
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
```
## notas adicionales
hacer que la opción b llame a imprimir bandera
## referencias
