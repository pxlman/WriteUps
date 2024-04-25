# Description
Can you find the flag in file without running it?

# Solving
First of all let's see the filetype and check what we can do
```
$ file strings                  
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=0cdedfba33422d235dba8c90e00fb77b235f1ff8, not stripped
                                                                                                               
$ ./strings
zsh: permission denied: ./strings
                                                                                                               
$ chmod +x strings
                                                                                                               
$ ./strings
Maybe try the 'strings' function? Take a look at the man page
```
no we can check the strings in the file using `strings`
```
$ strings strings
```
It gave me a whole bunch of text we can find what we need using grep
```
$ strings strings | grep pico 
picoCTF{5tRIng5_1T_7f766a23}
```
## GLAFHET
picoCTF{5tRIng5_1T_7f766a23}
