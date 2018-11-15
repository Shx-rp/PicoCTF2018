# picoCTF2018
PicoCTF 2018 solved by Shx &amp; Gal1leo


## HEEEEEEERE'S Johnny!

### Question
Okay, so we found some important looking files on a linux computer. Maybe they can be used to get a password to the process. Connect with nc 2018shell3.picoctf.com 38860. Files can be found here: passwd shadow.
### Hints
If at first you don't succeed, try, try again. And again. And again.
If you're not careful these kind of problems can really "rockyou".
### Answer
I runned passwd file in **John the Ripper** and got nothing then ran shadow file and after a while got **root:password1**
submited it to the indicated shell

### Flag
**picoCTF{J0hn_1$_R1pp3d_4e5aa29e}**
