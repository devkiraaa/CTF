Link thử thách: https://play.picoctf.org/practice/challenge/242?difficulty=1&page=5 </br>
Truy cập vào đường dẫn trong đề bài ta được flag. Tuy nhiên flag này đã bị mã hóa một số kí tự.</br>
<p>
  <img width="931" height="88" alt="image" src="https://github.com/user-attachments/assets/26fb267b-ee1d-4166-a8db-3ad5d31416ff" />
</p>
Nhìn nhanh thì các kí tự bị mã hóa cần chuyển về ASCII và bên trong của chr đang ở dạng hex, vì vậy trước hết ta chuyển hết các kí tự hex -> decimal. Sau đó sử dụng bảng mã ASCII để tra kí tự tương ứng.</br>
<p>
  <img width="871" height="606" alt="image" src="https://github.com/user-attachments/assets/b4a96cbf-72b3-4807-9f8f-d59b856401dd" />
</p>
Sau khi giải xong ta được flag hoàn chỉnh: picoCTF{gl17ch_m3_n07_bca68f75}.
