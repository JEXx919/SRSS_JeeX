## Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [dolls.jpg](https://challenge-files.cylabacademy.net/library/c48ba7ec3de5a7143687a4363cfa559846283c6f5b87de43d08de59aec195224/dolls.jpg)

Wait, you can hide files inside files? But how do you find them?

Make sure to submit the flag as academy{XXXXX}
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ unzip dolls.jpj
unzip:  cannot find or open dolls.jpj, dolls.jpj.zip or dolls.jpj.ZIP.

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ unzip dolls.jpj
unzip:  cannot find or open dolls.jpj, dolls.jpj.zip or dolls.jpj.ZIP.

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ls
base_images  dolls.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cd base_images

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images]
└─$ ls
2_c.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images]
└─$ unzip 2_c.jpg
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images]
└─$ ls
2_c.jpg  base_images

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images]
└─$ cd base_images

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images/base_images]
└─$ ls
3_c.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images/base_images]
└─$ unzip 3_c.jpg
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images/base_images]
└─$ ls
3_c.jpg  base_images

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images/base_images]
└─$ cd base_images

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images/base_images/base_images]
└─$ ls
4_c.jpg

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images/base_images/base_images]
└─$ unzip 4_c.jpg
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
 extracting: flag.txt

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images/base_images/base_images]
└─$ ls
4_c.jpg  flag.txt

┌──(jeex㉿LAPTOP-77F4GRAK)-[~/base_images/base_images/base_images]
└─$ cat flag.txt
academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
```

```
academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
```
## notas adicionales

## referencias
