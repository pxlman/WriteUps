# Description
Someone's commits seems to be preventing the program from working. Who is it? You can download the challenge files here:

    challenge.zip

# Solving
After extracting the file and going to the drop-in folder we find a messege.py with an incomplete code with a .git folder.
So i checked the git logs using `git log` and i found this in the logs
```
commit 8c83358c32daee3f8b597d2b853c1d1966b23f0a
Author: picoCTF{@sk_th3_1nt3rn_2c6bf174} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:11 2024 +0000

    optimize file size of prod code

```
## TheFlag
picoCTF{@sk_th3_1nt3rn_2c6bf174}
