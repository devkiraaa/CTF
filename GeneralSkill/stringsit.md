<img width="324" height="69" alt="image" src="https://github.com/user-attachments/assets/38f44425-54f9-4018-b980-51511ae0c949" />Link challenge https://play.picoctf.org/practice/challenge/37?difficulty=1&page=7
We dowload file in challenge.
wget + link file
And we have a file: strings
Structure of the flag: picoCTF{flag}
Read file and search flag with keyword "pico" : cat strings | grep "pico"
<img width="370" height="72" alt="image" src="https://github.com/user-attachments/assets/f4fd057b-a532-438c-98ae-db1d6323b88b" />
But this file has both text and binary, so use cat can't search flag.
We will use strings replace for cat: strings strings | grep "pico"
<img width="324" height="69" alt="image" src="https://github.com/user-attachments/assets/27eb9b47-bf66-466c-b093-aa3134f49146" />
The final, we finded the flag: picoCTF{5tRIng5_1T_A1b9ECAa}




