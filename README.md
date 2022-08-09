# umask
* https://askubuntu.com/questions/805862/how-to-change-umask-mode-permanently

## Set Default values
```
sudo vim /etc/login.defs
USERGROUPS_ENAB yes => change to USERGROUPS_ENAB no

ERASECHAR   0177
KILLCHAR    025
UMASK       027 => change the value

To set up a specific value for a user just add in 
cat<<EOF>> ~/.profile
umask 022
EOF
```

## Examples
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
