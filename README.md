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


## strings

### Question
Can you find the flag in this file without actually running it? You can also find the file in /problems/strings_2_b7404a3aee308619cb2ba79677989960 on the shell server.

### Hints
strings(Link)

### Answer
i opened strings file in notepad and just used the find to find a string that had picoCTF in it.

### Flag
**PicoCTF{sTrIngS_sAVeS_Time_3f712a28}**

## Inspect Me

### Question
Inpect this code! http://2018shell3.picoctf.com:47428

### Answer
inspected elements and found nothing then i inspected the sources and found theese:
*I learned HTML! Here's part 1/3 of the flag: picoCTF{ur_4_real_1nspe*
*I learned CSS! Here's part 2/3 of the flag: ct0r_g4dget_e96dd105}*

### Flag
**picoCTF{ur_4_real_1nspect0r_g4dget_e96dd105}**
