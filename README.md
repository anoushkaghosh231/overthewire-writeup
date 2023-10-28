# overthewire-writeup

<b> Level 12 to 13</b><br><br>
First we create a directory and copy the hexdump file data.txt onto the directory using mkdir and cp.
<br>![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/110865e4-41d6-458e-afbc-3c232b3d2f8c)
<br> Then we move to the directory we created and convert back the hexdump file to its original binary form as pw.
<br>![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/cb223dc2-6dce-45a8-8a2b-17144020d09c)
<br> Now, we repeatedly perform the following operations as the file is repeatedly compressed.
<br> (1) check the data type of the file;
<br> (2) rename the file according to file type
<br> (3) decompress using gunzip, gzip -d, bzip2 -d, tar xvf according to file type.
<br> We stop as soon as we get ASCII file type.
<br>![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/f292ab5b-d4e4-44d7-be9c-c3a4d20ea7b3)
<br>![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/d0cff6e5-c45b-4d7e-b4d2-c724236252c7)
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/edd64cb9-8bfd-4364-90ee-a96c468291d7)
_______________________________________________________________________________
<br>
<b> Level 13 to 14 </b>

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/57818bc8-641b-4006-add3-a97dbd856dfd)

<br> We use ssh private key to enter the bandit14 without using password. Command used is ssh -i to connect a remote machine to the server, then read the password from /etc/bandit_pass/bandit14
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/53b28f01-4e12-4a93-9d2a-1398ceaff997)
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/0e61e769-c3e0-40d5-b7a6-6dbf67795b9d)
<br>
_____________________________________________________________________________________
<br>
<b>Level 14 to 15 </b>
<br> Connecting to localhost at port 30000 using telnet. Entering the current password to get the new password.

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/5ca614d5-4bca-46ab-9c58-228a1438a434)

<br> 
____________________________________________________________________________________________________

<br>
<b> Level 15 to 16</b>
<br> Using openssl s_client to connect to localhost at port 30001; ign_eof to signify end of file.

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/80683999-b200-4196-824c-acc05d399821)
<br> Entering the current password to get the new password.
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/8f107628-2aa2-4334-8e45-097bb14f7ccb)
<br>
___________________________________________________________________________________________
<br>
<b>Level 16 to 17</b>
<br> We search for listening ports through port scanner nmap and specifying the range.

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/03c90889-1a44-4fdd-b566-7f2cc620f23d)
<br> Then we check for the recieved ports one by one, out of which port 31790 gives back RSA Private Key on entering password.
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/df924951-465a-4eb2-9cb6-175ecf2e7437)
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/1ac5559f-8d02-4e91-9217-788f50f9c41a)
![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/f393f955-6263-4b41-bc6b-260cded1d1ca)
<br> We save this RSA Private Key in a file bandit17.key. 
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/52104752-7140-4b4e-813d-8929aea644b9)
<br> We further secure the key file using chmod and changing the access, otherwise the key file will not get utilized. Then we use ssh -i to enter bandit17 using RSA Private Key.
![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/53ea79d2-cf62-45da-acea-56541d4388d8)
______________________________________________________________________________________________
<br>
<b>Level 17 to 18</b>
<br> diff command specifies the differences in the contents of both the files.

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/a2b1f489-ab01-454d-bd98-b2fdd5818e8b)
___________________________________________________________________________________________
<br>
<b>Level 18 to 19</b>
<br> ssh -t is used to make a silent connection as if the terminal is a hardware, and hence is known pseudo terminal

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/d8201a61-0d9f-4e70-b583-64e2334d4eda)
_____________________________________________________________________________________________
<br>
<b> Level 19 to 20 </b>
<br> using bandit20-do to run executable commands and read the password from the known directory.

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/0853c2a7-27b7-4b07-b283-ede99e0abb9c)
_______________________________________________________________________________________________
<br>
<b> Level 20 to 21</b>
<br> We use 2 terminals in this level to send the password through netcat at port 5000.

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/b65253ef-86ea-4613-99da-9d0999ddd386)

<br> And the receive through uid suconnect at port 5000.
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/4f61de76-fb02-4720-b603-da79ac753a8e)
______________________________________________________________________________________________
<br>
<b>Level 21 to 22</b>
<br> We enter the specified directory

<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/bf84df68-fe4b-4b81-8c62-e3a33d455085)
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/c6feb404-78fa-443c-a9bd-2a59bf805906)
<br> We then read the file cronjob_bandit22 using cat. This gives us a location of a file.
<br> On reading this location, we get another file location. This file has the password.
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/254b6fe4-e642-4eed-8f7b-c88d490585a3)
___________________________________________________________________________________________
