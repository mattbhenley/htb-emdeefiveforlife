# htb-emdeefiveforlife
hack the box web challenge 

First, we start the instance and are met with this screen in the browser:

![emdee1](https://github.com/mattbhenley/Images/blob/master/emdeefive.png)

This is asking you to MD5 encrypt the provided string. However, no matter how fast you encrypt and then submit, it gives the alert “Too slow!”. 

I then thought that executing a python script on my machine might be the fastest way to encrypt the message and receive the flag. 

This is the script I used to extract the encrypted string: 

-re module - for regex
-hashlib - for MD5
-requests module - for GET and POST

![emdee2](https://github.com/mattbhenley/Images/blob/master/emdeefivepython.png)

So this script essentially targets the URL, grabs the string from “h3 align=‘center” and encrypts it. It then returns the result in text in the “p align=center” where our message “Too slow!” initially was. {HTB Flag: HTB{N1c3_ScrIpt1nG_B0i!}
