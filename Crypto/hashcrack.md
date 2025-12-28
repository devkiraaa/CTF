Link thử thách: https://play.picoctf.org/practice/challenge/475?difficulty=1&page=1 </br>
Ta dùng nc truy cập vào địa chỉ của thử thách ta được
<p><img width="493" height="112" alt="image" src="https://github.com/user-attachments/assets/d4e2be95-a913-4ae6-a97e-8ed19c46793a" />
</p>
Theo hình ảnh ta thấy có một hàm băm 32 ký tự -> MD5 xuất hiện -> giải hàm băm này để có được mật khẩu
<p>
  <img width="925" height="336" alt="image" src="https://github.com/user-attachments/assets/5f0834dc-46c1-4d2a-8b21-40a365a80beb" />
</p>
Tạo 1 file hash.txt chứa hàm băm MD5. Sau đó tiến hành Hashcat với Direction Attach. </br>
hashcat -m 0 -a 0 hash.txt /usr/share/wordlists/rockyou.txt với rockyou.txt là 1 file chứa mật khẩu nổi tiếng trên Kali Linux. </br>
<p>
  <img width="390" height="69" alt="image" src="https://github.com/user-attachments/assets/4b683519-9d6e-485f-8db5-82750a5c568a" />
</p>
Tiến hành show mật khẩu ta được password123. Nhập password ta được 1 hàm băm mới cần giải để nhập mật khẩu cho cổng thứ 2. </br>
<p>
  <img width="744" height="181" alt="image" src="https://github.com/user-attachments/assets/8c0f6407-76c5-4e89-b570-d03ea92f2dd2" />
</p>
Ở đây ta thấy một hàm băm mới có 40 ký tự Hex -> Mã SHA-1 -> giải hàm băm này để lấy mật khẩu </br>
<p>
  <img width="521" height="43" alt="image" src="https://github.com/user-attachments/assets/bc58b214-addf-431f-a967-c0d9dc43ea06" />
</p>
Tạo một file hash1.txt để chứa hàm băm SHA-1. Sau đó giải file này. </br>
Dùng lệnh hashcat -m 100 -a 0 hash1.txt /usr/share/wordlists/rockyou.txt. </br>
<p>
  <img width="942" height="692" alt="image" src="https://github.com/user-attachments/assets/1822f39c-7832-4b46-a521-884a7e3f55f7" />
</p>
Ta được mật khẩu là letmein. Nhập mật khẩu ta sang cổng tiếp theo với một hàm băm mới. </br>
<p>
  <img width="842" height="109" alt="image" src="https://github.com/user-attachments/assets/28f87a48-063d-4039-bab5-b0e8cf44a909" />
</p>
Ta thấy hàm băm mới có 256 ký tự Hex -> SHA-256 -> Giải hàm băm này.</br>
Trước hết tạo 1 file hash2.txt chứa hàm băm này. Sau đó cần giải mã hàm băm này 

