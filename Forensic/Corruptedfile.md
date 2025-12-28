Link thử thách: https://play.picoctf.org/practice/challenge/519?difficulty=1&page=1 </br>
Tải file về ta được 1 tệp tên là file. Dựa vào gợi ý của đề bài ta thấy file gốc là 1 file ảnh định dạng JPEG. Tuy nhiên thì khi kiểm tra tiêu đề của file thì ta nhận thấy không đúng định dạng tiêu đề file JPEG. Như hình bên dưới. </br>
<p>
  <img width="645" height="80" alt="image" src="https://github.com/user-attachments/assets/bcb7cba2-96bc-4dbc-9013-3dbc939afafd" />
</p>
Ta thấy sự bất thường 2 byte đầu. Nên ta sẽ chỉnh sửa tiêu đề file để đưa về đúng định dạng file. </br>
<p>
  <img width="403" height="56" alt="image" src="https://github.com/user-attachments/assets/18458e13-e424-4431-a4e1-4fb63649c7e4" />
</p>
Tiến hành kiểm tra lại tiêu đề file, ta thấy đã đúng định dạng </br>
<p>
  <img width="661" height="85" alt="image" src="https://github.com/user-attachments/assets/3d5bfcce-d473-4f87-ac02-bee8685f99fa" />
</p>
Đổi lại tên file ảnh. </br>
<p>
  <img width="228" height="57" alt="image" src="https://github.com/user-attachments/assets/395490e3-7f22-4116-ace9-b3a5701c014b" />
</p>
Mở lại file và kiểm tra. Ta được flag: picoCTF{r3st0r1ng_th3_by73s_939a65f5} </br>
<p>
  <img width="799" height="497" alt="image" src="https://github.com/user-attachments/assets/7c0d4448-90a0-4070-bcbd-96e719dd6667" />
</p>
