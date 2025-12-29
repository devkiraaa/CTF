Link thử thách: https://play.picoctf.org/practice/challenge/460?difficulty=1&page=2 </br>
Tiến hành tải file về ta được 1 file ảnh có tên là red.PNG, mở file ảnh lên xem thì thấy toàn màu đỏ nên chắc không khai thác được gì.</br>
<p>
  <img width="946" height="851" alt="image" src="https://github.com/user-attachments/assets/4d8c0abd-2f61-487a-b95a-db12055a86c2" />
</p>
Thoi thì thử check thông tin cái ảnh xem có gì. Dùng exiftool nhé.</br>
<p>
<img width="940" height="424" alt="Screenshot 2025-12-29 084756" src="https://github.com/user-attachments/assets/f2c3506e-2f1e-4e9d-b13e-8e24d293744c" />
</p>
Ở thẻ Poem thấy có nhiều chữ quá mà ngu tiếng anh nên không biết phải làm sao:v</br>
Ngồi nghĩ một lúc thì thấy nếu chỉ lấy các chữ cái viết hoa ghép lại thì ta được CHECKLSB!!! </br> 
</br>
Hmm đây là gợi ý vô cùng quan trọng đấy. Nó gợi ý cho ta nên kiểm tra LSB.
Cùng tìm hiểu xem LSB là gì nhé?  LSB là viết tắt của Least Significant Bit (Bit ít quan trọng nhất). Hiểu đơn giản một file ảnh sẽ có MSB(Most Significant Bit) - Bit quan trọng nhất và nằm ở các các bit đầu bên trái. Ngược lại LSB nằm bên phải. Khi thay đổi các giá trị MSB thì ta có thể nhận thấy dễ dàng sự thay đổi của ảnh. Tuy nhiên nếu thay đổi LSB thì gần như không thể nhận ra sự thay đổi của màu sắc. Lợi dùng điều này người ta thường sẽ giấu tin trong các bit này để không bị phát hiện.</br>
Để kiểm tra LSB ta có thể sử dụng stegsolve hoặc zsteg. Trong bài này mình sẽ dùng zsteg.</br>
<p>
  <img width="194" height="41" alt="image" src="https://github.com/user-attachments/assets/cd4bde61-65df-4858-8697-74b28391652f" />
</p
Sau đó ta nhận được kết quả như hình dưới.</br>
<p>
  <img width="934" height="389" alt="image" src="https://github.com/user-attachments/assets/0ff0b899-e5ef-4287-a5cb-6eee800540a7" />
</p>
Ta thấy chuỗi kí tự bất thường có sự lặp lại chuỗi kí tự nên thử decode xem được gì nhé. </br>
<p>
  <img width="936" height="102" alt="image" src="https://github.com/user-attachments/assets/7cc015f4-cea4-4ffd-b08e-408ca323aa93" />
</p>
Sau khi decode thì ra cờ luôn:v flag: picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}
<p>
  <img width="933" height="152" alt="image" src="https://github.com/user-attachments/assets/6f15d9ed-7788-4e86-83a5-6e4c3c6baa46" />
</p>
