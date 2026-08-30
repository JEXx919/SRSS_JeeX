## Descripcion
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_titan/70/challenge.zip)
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c_titan/70/challenge.zip
--2026-08-30 05:37:05--  https://artifacts.picoctf.net/c_titan/70/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24662 (24K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                   100%[=====================================================================================================>]  24.08K  --.-KB/s    in 0.01s   

2026-08-30 05:37:06 (2.25 MB/s) - 'challenge.zip' saved [24662/24662]

JeeX7ZaZ-academy@webshell:~$ 



JeeX7ZaZ-academy@webshell:~$ git log
fatal: not a git repository (or any parent up to mount point /)
Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).
JeeX7ZaZ-academy@webshell:~$ git branch -a
fatal: not a git repository (or any parent up to mount point /)
Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).
JeeX7ZaZ-academy@webshell:~$ cd
Display all 3264 possibilities? (y or n)
JeeX7ZaZ-academy@webshell:~$ ls
challenge.zip  drop-in
JeeX7ZaZ-academy@webshell:~$ cd drop-in
JeeX7ZaZ-academy@webshell:~/drop-in$ git lof
git: 'lof' is not a git command. See 'git --help'.

The most similar command is
        log
JeeX7ZaZ-academy@webshell:~/drop-in$ git log
JeeX7ZaZ-academy@webshell:~/drop-in$ ls
flag.py
JeeX7ZaZ-academy@webshell:~/drop-in$ nano flag.py
JeeX7ZaZ-academy@webshell:~/drop-in$ git log
JeeX7ZaZ-academy@webshell:~/drop-in$ git checkout 54c7842e34d03976ddc080a9dd76742751024358
Note: switching to '54c7842e34d03976ddc080a9dd76742751024358'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 54c7842 init flag printer
JeeX7ZaZ-academy@webshell:~/drop-in$ nano flag.py
JeeX7ZaZ-academy@webshell:~/drop-in$ python3 flag.py
Printing the flag...







JeeX7ZaZ-academy@webshell:~/drop-in$ git log
JeeX7ZaZ-academy@webshell:~/drop-in$ git branch -a
JeeX7ZaZ-academy@webshell:~/drop-in$ git config part 2
error: key does not contain a section: part
JeeX7ZaZ-academy@webshell:~/drop-in$ git checkout feature/part-1
Previous HEAD position was 54c7842 init flag printer
Switched to branch 'feature/part-1'
JeeX7ZaZ-academy@webshell:~/drop-in$ nano flag.py
JeeX7ZaZ-academy@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
JeeX7ZaZ-academy@webshell:~/drop-in$ nano flag.py
JeeX7ZaZ-academy@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
JeeX7ZaZ-academy@webshell:~/drop-in$ nano flag.py
JeeX7ZaZ-academy@webshell:~/drop-in$ 

python parte 1
  GNU nano 6.2                                                                                flag.py                                                                                         
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')


parte 2
  GNU nano 6.2                                                                                flag.py                                                                                         
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')



parte 3
  GNU nano 6.2                                                                                flag.py                                                                                         
print("Printing the flag...")

print("w0rk_7ffa0077}")






```

```
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ffa0077}
```
## notas adicionales

## referencias
[The CTF Primer](https://primer.picoctf.org/#_git_version_control)
[Webshell](https://webshell.cylabacademy.org/)
[Google Gemini](https://gemini.google.com/app)