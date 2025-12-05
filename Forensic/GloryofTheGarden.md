Link challenge: https://play.picoctf.org/practice/challenge/44?difficulty=1&page=7
We get the flag from imagine
Dowload the imagine:
wget + link imagine
After dowloaded, we had a file garden.jpg
Read file and search the flag: cat garden.jpg | grep "pico"
but file has text and binary. '
<img width="369" height="69" alt="image" src="https://github.com/user-attachments/assets/fd4a6432-0eb1-4d20-b3a4-3f5da464487d" />
So, we use strings to search: strings garden.jpg | grep "pico" 
<img width="484" height="71" alt="image" src="https://github.com/user-attachments/assets/fed1d20d-49e5-4493-9a5e-d456c2dfdfb4" />
Flag: picoCTF{more_than_m33ts_the_3y395e12915}





