# Description
Cryptography can be easy, do you know what ROT13 is? 
  cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_uJdSftmh}

# Solving
I know that this encryption shifts any character by 13 in the alphabet wheel
So we gonna use tr
```
$ echo "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_uJdSftmh}" | tr "a-zA-Z" "n-za-mN-ZA-M"
picoCTF{next_time_I'll_try_2_rounds_of_rot13_hWqFsgzu}
```
## Note
the flag contains lower and uppercase letters which means we must add this to the tr command
