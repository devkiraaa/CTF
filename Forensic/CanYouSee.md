Link thử thách: https://play.picoctf.org/practice/challenge/408?difficulty=1&page=4</br>
Tiến hành tải file của thử thách.</br>
<p>
  <img width="943" height="227" alt="image" src="https://github.com/user-attachments/assets/f8dd7113-5cde-49f1-9c39-c6701a33fd68" />
</p>
Ta được 1 file định dạng .zip -> Ta cần giải nén file này.</br>
<p>
  <img width="322" height="98" alt="image" src="https://github.com/user-attachments/assets/5f9ba9fa-2985-41da-a65d-296e97fb896b" />
</p>
Sau khi giải nén ta được 1 file ảnh định dạng .jpg. Tiến hành kiểm tra thông tin file này. </br>
<p>
  <img width="702" height="448" alt="image" src="https://github.com/user-attachments/assets/8e25f034-3a57-464d-8edf-31cc7e9c18a5" />
</p>
Chú ý ở thẻ Attribution URL ta thấy có chuỗi kí tự lạ khả năng bị mã hóa base64. Vì vậy thử decode chuỗi đó xem được gì không.</br>
<p>
  <img width="588" height="76" alt="image" src="https://github.com/user-attachments/assets/4b6a5524-98e1-480e-9e07-093f6eb2b3b9" />
</p>
Ồ!!! Ra flag nè: picoCTF{ME74D47A_HIDD3N_3b9209a2}.
