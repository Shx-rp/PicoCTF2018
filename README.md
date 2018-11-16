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

## Irish Name Repo

### Question
There is a website running at http://2018shell3.picoctf.com:59464 (link). Do you think you can log us in? Try to see if you can login!

### Answer
after opening the page it had a admin login so i performed a simple **SQL injection** and logged in

### Flag
**picoCTF{con4n_r3411y_1snt_1r1sh_d121ca0b}**

### Mr. Robots

### Question
Do you see the same things I see? The glimpses of the flag hidden away? http://2018shell3.picoctf.com:15298 (link) 

## Answer
This time there is no login page so i looked at the name and noticed it said robots and immediatelly thought of **robots.txt**
i set the url to http://2018shell3.picoctf.com:15298/robots.txt
and noticed that in the disallow message it had a .html url
i set it to that url and got the flag

### Flag
**picoCTF{th3_w0rld_1s_4_danger0us_pl4c3_3lli0t_c4075}**

## Truly an Artist

### Question
Can you help us find the flag in this Meta-Material? You can also find the file in /problems/truly-an-artist_2_61a3ed7216130ab1c2b2872eeda81348. 

### Answer
the file was a picture and also the question gave us a hint at what to do so for that i examined the Metadata and EXIF files of the pic
and in the Artist label there was the flag

### Flag
**picoCTF{look_in_image_7e31505f}**
