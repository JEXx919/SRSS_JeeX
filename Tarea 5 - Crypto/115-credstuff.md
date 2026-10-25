## Descripción
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://challenge-files.cylabacademy.net/library/7f760cee144ac7237469fd6bfab7c748d6f1d101ca47c101187ca7d8f5c721f0/leak.tar).

The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

Maybe other passwords will have hints about the leak?
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ tar -xvf leak.tar
leak/
leak/passwords.txt
leak/usernames.txt

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/leak]
└─$ ls
passwords.txt  usernames.txt

-- cd -

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ grep -ni 'cultiris' leak/usernames.txt
378:cultiris

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ sed -n '378p' leak/passwords.txt
npnqrzl{P7e1S_54I35_71Z3}

npnqrzl{P7e1S_54I35_71Z3}
ROT 13
academy{C7r1F_54V35_71M3}


```

```
academy{C7r1F_54V35_71M3}
```
## notas adicionales

## referencias
[ROT13 - CyberChef](https://gchq.github.io/CyberChef/#recipe=ROT13\(true,true,false,13\)&input=bnBucXJ6bHtQN2UxU181NEkzNV83MVozfQ)