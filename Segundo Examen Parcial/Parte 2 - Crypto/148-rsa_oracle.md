## Descripción
Can you abuse the oracle?

An attacker was able to intercept communications between a bank and a fintech company. They managed to get the [message](https://challenge-files.cylabacademy.net/library/c160444b2e2c0d9b093294670f0feec4d0e65abfcfc56e9524fb337c65cb9110/secret.enc) (ciphertext) and the [password](https://challenge-files.cylabacademy.net/library/c160444b2e2c0d9b093294670f0feec4d0e65abfcfc56e9524fb337c65cb9110/password.enc) that was used to encrypt the message. After some intensive reconassainance they found out that the bank has an oracle that was used to encrypt the password and can be found here `nc xebec.cylabacademy.net 25918`. Decrypt the password and use it to decrypt the message. The oracle can decrypt anything except the password.

Crytography Threat models: chosen plaintext attack.

OpenSSL can be used to decrypt the message. e.g `openssl enc -aes-256-cbc -d ...`

The key to getting the flag is by sending a custom message to the server by taking advantage of the RSA encryption algorithm.

Minimum requirements for a useful cryptosystem is CPA security.
## solución 
```

- Se descargaron e inspeccionaron los archivos `password.enc` y `secret.enc`.
    
- **Criptoanálisis (RSA Blinding / Ataque de Cifrado Elegido):**
    
    - Dado que el oráculo rechaza descifrar directamente el archivo `password.enc`, se aprovechó la propiedad homomórfica (maleabilidad) de RSA.
        
    - Se multiplicó el criptograma original por $2^e$ (donde $e = 65537$) para generar un criptograma alterado que el oráculo descifró sin restricciones.
        
    - Al dividir el texto claro devuelto por 2, se recuperó la contraseña original: `4263a`.
        
- **Descifrado del Archivo:**
    
    - Se utilizó la herramienta OpenSSL con el algoritmo AES-256-CBC y la contraseña extraída para descifrar `secret.enc`:
        
        Bash
        
        ```
        openssl enc -aes-256-cbc -d -in secret.enc -pass pass:4263a
        ```
        
- **Bandera:** Obtenida mediante el texto plano resultante del descifrado de OpenSSL.
```

```
academy{su((3ss_(r@ck1ng_r3@_88a127f1}
```
## notas adicionales
- **Maleabilidad de RSA (CWE-321):** El cifrado RSA sin esquemas de relleno apropiados (como OAEP) permite que un atacante modifique un criptograma y obtenga una relación matemática predecible en el texto claro resultante, invalidando la confidencialidad si se dispone de un oráculo de descifrado activo.
## referencias
- Reto original: picoCTF 2024 - Categoría: Cryptography (Medium).
    
- Autor: Geoffrey Njogu.
    
- Conceptos aplicados: RSA Blinding, Cifrado Homomórfico, Criptoanálisis de Oráculos, Descifrado Simétrico AES-256-CBC.