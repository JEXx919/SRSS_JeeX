## Descripción
Download this disk image, find the key and log into the remote machine.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://challenge-files.cylabacademy.net/library/32b4f7450d7368e22562f75fed35fecd7bdfa2172559a90a42a149e27d781464/disk.img.gz)
- Remote machine: `ssh -i key_file -p 48093 ctf-player@chatelaine.cylabacademy.net`
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cd /tmp

┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ wget https://challenge-files.cylabacademy.net/library/32b4f7450d7368e22562f75fed35fecd7bdfa2172559a90a42a149e27d781464/disk.img.gz
--2026-10-07 23:27:59--  https://challenge-files.cylabacademy.net/library/32b4f7450d7368e22562f75fed35fecd7bdfa2172559a90a42a149e27d781464/disk.img.gz
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.66, 13.226.187.37, 13.226.187.22, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 48132743 (46M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                                  100%[==============================================================================================>]  45.90M  2.49MB/s    in 22s

2026-10-07 23:28:22 (2.08 MB/s) - ‘disk.img.gz’ saved [48132743/48132743]




┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ ls -lh disk.img.gz
-rw-r--r-- 1 jeex jeex 46M Sep 22 20:58 disk.img.gz

┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ gunzip disk.img.gz

┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ ls -lh disk.img
-rw-r--r-- 1 jeex jeex 230M Sep 22 20:58 disk.img

┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ ls -lh /tmp/disk.img
-rw-r--r-- 1 jeex jeex 230M Sep 22 20:58 /tmp/disk.img

┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ file disk.img
disk.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x83, start-CHS (0xc,223,20), end-CHS (0x1d,81,52), startsector 206848, 264192 sectors


fdisk -l disk.img
┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ fdisk -l disk.img
Disk disk.img: 230 MiB, 241172480 bytes, 471040 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0x0b0051d0

Device     Boot  Start    End Sectors  Size Id Type
disk.img1  *      2048 206847  204800  100M 83 Linux
disk.img2       206848 471039  264192  129M 83 Linux


┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ sudo losetup -Pf --show disk.img
/dev/loop0

┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ lsblk -f
NAME      FSTYPE FSVER LABEL UUID                                 FSAVAIL FSUSE% MOUNTPOINTS
loop0
├─loop0p1 ext4   1.0         e3b59046-994f-4513-bd8e-9b73b55f162a
└─loop0p2 ext4   1.0         12d9658c-565f-42de-be97-eb4bfbe21b9a
sda       ext4   1.0
sdb       ext4   1.0
sdc       swap   1           a3709db2-c289-4125-9d47-1eb2b0579385                [SWAP]
sdd       ext4   1.0         a543e02c-9cc0-4bc4-bcdd-f21775e82871  949.2G     1% /mnt/wslg/distro
                                                                                 /
                                                                                 
                                                                                 
                                                                                 
                                                                                 

┌──(jeex㉿LAPTOP-77F4GRAK)-[/tmp]
└─$ ssh -i /tmp/key_file -p 26547 ctf-player@xebec.cylabacademy.net
Welcome to Ubuntu 24.04.4 LTS (GNU/Linux 7.0.0-1014-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt
academy{k3y_5l3u7h_f52dbc2c}ctf-player@challenge:~$

```

```
academy{k3y_5l3u7h_f52dbc2c}
```

## notas adicionales

## referencias
