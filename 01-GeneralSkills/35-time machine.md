## Descripcion
What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:


The `cat` command will let you read a file, but that won't help you here!

Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).

When committing a file with git, a message can (and should) be included.
## solucion 
```
JeeX7ZaZ-academy@webshell:~$ wget https://artifacts.picoctf.net/c_titan/68/challenge.zip
--2026-08-30 05:13:59--  https://artifacts.picoctf.net/c_titan/68/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.95, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17738 (17K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                   100%[=====================================================================================================>]  17.32K  --.-KB/s    in 0.007s  

2026-08-30 05:13:59 (2.50 MB/s) - 'challenge.zip' saved [17738/17738]

JeeX7ZaZ-academy@webshell:~$ ls
challenge.zip
JeeX7ZaZ-academy@webshell:~$ unzip challenge.zip
Archive:  challenge.zip
   creating: drop-in/
  inflating: drop-in/message.txt     
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
   creating: drop-in/.git/objects/25/
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
   creating: drop-in/.git/objects/70/
 extracting: drop-in/.git/objects/70/5ff639b7846418603a3272ab54536e01e3dc43  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
JeeX7ZaZ-academy@webshell:~$ 


JeeX7ZaZ-academy@webshell:~$ ls
challenge.zip  drop-in
JeeX7ZaZ-academy@webshell:~$ cd drop-in
JeeX7ZaZ-academy@webshell:~/drop-in$ ls
message.txt
JeeX7ZaZ-academy@webshell:~/drop-in$ cat message.txt
This is what I was working on, but I'd need to look at my commit history to know why...JeeX7ZaZ-academy@webshell:~/drop-in$ git log
-----------------------------------------------------------------------------
commit 705ff639b7846418603a3272ab54536e01e3dc43 (HEAD, master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:36 2024 +0000

    picoCTF{t1m3m@ch1n3_b476ca06}
(END)



-----------------------------------------------------------------------------
JeeX7ZaZ-academy@webshell:~/drop-in$ git checkout 705ff639b7846418603a3272ab54536e01e3dc43
Note: switching to '705ff639b7846418603a3272ab54536e01e3dc43'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 705ff63 picoCTF{t1m3m@ch1n3_b476ca06}
JeeX7ZaZ-academy@webshell:~/drop-in$ 


```

```
picoCTF{t1m3m@ch1n3_b476ca06}
```
## notas adicionales
aqui directamente al ejecutar git log se nos muestra la bandera que esta en el historial de commits, y hacer un git checkout de igual manera nos muestra la bandera.
## referencias
[El Resumen de la CTF](https://primer.picoctf.org/#_git_version_control)
[Webshell](https://webshell.cylabacademy.org/)