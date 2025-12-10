Link challenge: https://play.picoctf.org/practice/challenge/68?difficulty=1&page=6
Dowload this file we have a image:
<img width="787" height="441" alt="image" src="https://github.com/user-attachments/assets/71210cc5-479f-46c3-a815-13073bda9820" />
Accoording to the hint, the flag is in the format PICOCTF{flag}
The imagine has strings of number. So we think that we decode them from decimal to charcode of ASCII
<img width="354" height="456" alt="image" src="https://github.com/user-attachments/assets/400d4408-f8e1-4068-ab8b-8d790dbabdbd" />
16 9 3 15 3 20 6 -> P I C O C T F. However, check  the table of ASCII we look them wrong.
But each number, we add 64 and check it right.
Final, we have rule. Each number + 64 and check in the table of ASCII.
PICOCTF{THENUMBERSMASON}
