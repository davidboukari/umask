# umask
```
right max
file: 666
direcctory: 777

umask set the default right
ex: 

umask 022
touch file
touch dir
file: 666 - 022 => 422
dir: 777 - 022 => 755

umask 027
file: 640
dir:  740

```
