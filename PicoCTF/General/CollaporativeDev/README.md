# Description
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together? You can download the challenge files here:

    challenge.zip

# Solving
we found a unhelpful python script and a .git folder
```
$ cat flag.py                                                                                 
print("Printing the flag...")

```
So we check the git logs
```
$ git log 
commit eb19d0e3c28278752f0735c4451b885136a24105 (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    init flag printer

```
So that's unhelpful, so let's check if is there any other branch
```
$ git branch   
  feature/part-1
  feature/part-2
  feature/part-3
* main
```
Now i think the flag is separated to three parts let's check each branch
- Part-1
```
$ git checkout feature/part-1 
Switched to branch 'feature/part-1'
                                                                                                               
$ git log flag.py 
commit 0cd57e0aedc31a1a92e0b79235c818de437cde8e (HEAD -> feature/part-1)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    add part 1

commit eb19d0e3c28278752f0735c4451b885136a24105 (main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    init flag printer
                                                                                                               
$ git show 0cd57e0aedc31a1a92e0b79235c818de437cde8e
commit 0cd57e0aedc31a1a92e0b79235c818de437cde8e (HEAD -> feature/part-1)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    add part 1

diff --git a/flag.py b/flag.py
index 77d6cec..6e17fb3 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,2 @@
 print("Printing the flag...")
+print("picoCTF{t3@mw0rk_", end='')
\ No newline at end of file
```
Part-1 : picoCTF{t3@mw0rk_

- Part-2
```
$ git checkout feature/part-2                      
Switched to branch 'feature/part-2'
                                                                                                               
$ git log flag.py            
commit 7064732e2fd39d2247bd6ba2ccc4cf9576974d38 (HEAD -> feature/part-2)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    add part 2

commit eb19d0e3c28278752f0735c4451b885136a24105 (main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    init flag printer
                                                                                                               
$ git show 7064732e2fd39d2247bd6ba2ccc4cf9576974d38
commit 7064732e2fd39d2247bd6ba2ccc4cf9576974d38 (HEAD -> feature/part-2)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    add part 2

diff --git a/flag.py b/flag.py
index 77d6cec..7ab4e25 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,3 @@
 print("Printing the flag...")
+
+print("m@k3s_th3_dr3@m_", end='')
\ No newline at end of file

```
Part-2: m@k3s_th3_dr3@m_

- Part-3
```
$ git checkout feature/part-3                      
Switched to branch 'feature/part-3'
                                                                                                               
$ git log flag.py            
commit 8395824cc0ce486d1be9ab874bfedb2cec2ea398 (HEAD -> feature/part-3)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    add part 3

commit eb19d0e3c28278752f0735c4451b885136a24105 (main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    init flag printer
                                                                                                               
$ git show 8395824cc0ce486d1be9ab874bfedb2cec2ea398
commit 8395824cc0ce486d1be9ab874bfedb2cec2ea398 (HEAD -> feature/part-3)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    add part 3

diff --git a/flag.py b/flag.py
index 77d6cec..4672a5c 100644
--- a/flag.py
+++ b/flag.py
@@ -1 +1,3 @@
 print("Printing the flag...")
+
+print("w0rk_2c91ca76}")

```
Part-3: w0rk_2c91ca76}


## FLAGTHE
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_2c91ca76}

