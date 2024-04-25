# Description
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.

# Solving
From the desctiption we can pridect it's a base64 encode but let's check this out

```
$ echo bDNhcm5fdGgzX3IwcDM1 | base64 -d                                                     
l3arn_th3_r0p35
```
It looks like a flag to me

## FLAG
PicoCTF{l3arn_th3_r0p35}
