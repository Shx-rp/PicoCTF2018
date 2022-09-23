# picoCTF2018
PicoCTF 2018 solved by Shx &amp; Gal1leo


## HEEEEEEERE'S Johnny! (Forensics)

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


## strings (General Skills)

### Question
Can you find the flag in this file without actually running it? You can also find the file in /problems/strings_2_b7404a3aee308619cb2ba79677989960 on the shell server.

### Hints
strings(Link)

### Answer
i opened strings file in notepad and just used the find to find a string that had picoCTF in it.

### Flag
**PicoCTF{sTrIngS_sAVeS_Time_3f712a28}**

## Inspect Me (Web exploitation)

### Question
Inpect this code! http://2018shell3.picoctf.com:47428

### Answer
inspected elements and found nothing then i inspected the sources and found theese:
*I learned HTML! Here's part 1/3 of the flag: picoCTF{ur_4_real_1nspe*
*I learned CSS! Here's part 2/3 of the flag: ct0r_g4dget_e96dd105}*

### Flag
**picoCTF{ur_4_real_1nspect0r_g4dget_e96dd105}**

## Irish Name Repo (web exploitation)

### Question
There is a website running at http://2018shell3.picoctf.com:59464 (link). Do you think you can log us in? Try to see if you can login!

### Answer
after opening the page it had a admin login so i performed a simple **SQL injection** and logged in

### Flag
**picoCTF{con4n_r3411y_1snt_1r1sh_d121ca0b}**

### Mr. Robots (Web exploitation)

### Question
Do you see the same things I see? The glimpses of the flag hidden away? http://2018shell3.picoctf.com:15298 (link) 

## Answer
This time there is no login page so i looked at the name and noticed it said robots and immediatelly thought of **robots.txt**
i set the url to http://2018shell3.picoctf.com:15298/robots.txt
and noticed that in the disallow message it had a .html url
i set it to that url and got the flag

### Flag
**picoCTF{th3_w0rld_1s_4_danger0us_pl4c3_3lli0t_c4075}**

## Truly an Artist (Forensics)

### Question
Can you help us find the flag in this Meta-Material? You can also find the file in /problems/truly-an-artist_2_61a3ed7216130ab1c2b2872eeda81348. 

### Answer
the file was a picture and also the question gave us a hint at what to do so for that i examined the Metadata and EXIF files of the pic
and in the Artist label there was the flag

### Flag
**picoCTF{look_in_image_7e31505f}**

## buttons (Web exploitation)

### Question
There is a website running at http://2018shell3.picoctf.com:18342 (link). Try to see if you can push their buttons. 

### Answer
Ok this one got me confused a bit in the beggining. i clicked on the first then the second and it trolled me. i got mad. after that i tried analysing the HTTP requests it made. i noticed that the first one made a POST request and the second one made a GET request
after sending a POST request in the second button it gave me a response. it was the flag

### Flag
**picoCTF{button_button_whose_got_the_button_25a99f84}**

## No Login (Web exploitation)

### Question
Looks like someone started making a website but never got around to making a login, but I heard there was a flag if you were the admin. http://2018shell3.picoctf.com:52920 (link) 

### Answer
so this one got me confused a lot. i tried SQL injections in the suposed login but it didnt even open. after i looked at the hints i noticed it was talking about cookies, and that it was looking for a admin value in them. i used a cookie editor to change it and made a session cookie that had the value admin=True and after clicking Flag it gave me it.

### Flag
**picoCTF{n0l0g0n_n0_pr0bl3m_3184f702}**

## Secret Agent (Web exploitation)

### Question
Here's a little website that hasn't fully been finished. But I heard google gets all your info anyway. http://2018shell3.picoctf.com:3827 (link)

### Answer
after opening it was another one without login so no SQL injections. after clicking flag it identefied my User Agent. so i tried changing My User agent to GoogleBot and it gave me the flag.

### Flag
**picoCTF{s3cr3t_ag3nt_m4n_12387c22}**

## The Vault (Web exploitation)

### Question
There is a website running at http://2018shell3.picoctf.com:53261 (link). Try to see if you can login! 

### Answer
this time there was a login page and so i tried some simple SQL injection commands and it worked

### Flag
**picoCTF{w3lc0m3_t0_th3_vau1t_23495366}**


## Super Secure Log In

### Question

### Answer
inspecting the source code u find the script that detects the password so that means that the password is beeing checked locally

"<script type="text/javascript">
  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(split*7, split*8) == '}') {
      if (checkpass.substring(split*6, split*7) == 'ebbd') {
        if (checkpass.substring(split*5, split*6) == 'd_d0') {
         if (checkpass.substring(split*4, split*5) == 's_ba') {
          if (checkpass.substring(split*3, split*4) == 'nt_i') {
            if (checkpass.substring(split*2, split*3) == 'clie') {
              if (checkpass.substring(split, split*2) == 'CTF{') {
                if (checkpass.substring(0,split) == 'pico') {
                  alert("You got the flag!")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
  }"
  
  ### Flag
  **picoCTF{client_is_bad_d0ebbd}**
  
  
  ## Logon
  
  ### Question
  
  ### Answer
  So i tried doing a SQLi but it didnt work and after taking a look at what the server was sending i realized that it sent a comment setting the flag "Admin=False" after the login so i turned it to "Admin=True" and after that it printed out the Flag
  
  ### Flag
  ***picoCTF{l0g1ns_ar3nt_r34l_a280e12c}***
