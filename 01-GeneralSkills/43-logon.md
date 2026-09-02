## Descripcion
The factory is hiding things from all of its users.
Can you login as Joe and find what they've been looking at? [http://fickle-tempest.picoctf.net:63090](http://fickle-tempest.picoctf.net:63090/)
  
Hmm it doesn't seem to check anyone's password, except for Joe's?

## solucion 

```
Iniciamos sesion con datos cualquiera y nos permite acceder //excepto con Joe.
al igresar...
Con ayuda de coockie-editor modificar la coockie de admin
que era False
y la cambiamos por True

```

```
picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}
```
## notas adicionales

## referencias
[Cookie-Editor - Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/cookieeditor/neaplmfkghagebokkhpjpoebhdledlfi)