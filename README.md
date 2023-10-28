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
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/9d2b908c-6b28-4b4c-81da-8fe6de4f4851)
<br> We use ssh private key to enter the bandit14 without using password. Command used is ssh -i to connect a remote machine to the server, then read the password from /etc/bandit_pass/bandit14
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/53b28f01-4e12-4a93-9d2a-1398ceaff997)
<br> ![image](https://github.com/anoushkaghosh231/overthewire-writeup/assets/109907350/0e61e769-c3e0-40d5-b7a6-6dbf67795b9d)
<br>
_____________________________________________________________________________________
<br>
<b>Level 14 to 15 </b>
<br> 
