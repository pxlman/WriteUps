# Description
Unzip this archive and find the file named 'uber-secret.txt'

    Download zip file

# Solving
After extracting i found many files to search in
```
$ tree .                                                                                    
.
├── 13771.txt.utf-8
├── 14789.txt.utf-8
├── acceptable_books
│   ├── 17879.txt.utf-8
│   ├── 17880.txt.utf-8
│   └── more_books
│       └── 40723.txt.utf-8
├── adequate_books
│   ├── 44578.txt.utf-8
│   ├── 46804-0.txt
│   └── more_books
│       ├── 1023.txt.utf-8
│       └── .secret
│           └── deeper_secrets
│               └── deepest_secrets
│                   └── uber-secret.txt
└── satisfactory_books
    ├── 16021.txt.utf-8
    ├── 23765.txt.utf-8
    └── more_books
        └── 37121.txt.utf-8

10 directories, 12 files

```
So i used `grep -r`
```
$ grep -r picoCTF{
adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}
```
## FLAG
picoCTF{f1nd_15_f457_ab443fd1}
