Link thử thách: https://play.picoctf.org/practice/challenge/523?difficulty=1&page=1 </br>
Ta có 1 file tiến hành tải file và check ta thấy toàn bộ nội dung file đều bị mã hõa bởi base64. Sử dụng công cụ CyberChef để decode file. </br>
<p>
  <img width="709" height="730" alt="image" src="https://github.com/user-attachments/assets/99686c1c-2452-453e-b01f-00c8d6d1bed3" />
</p>
Sau khi decode xong thì thì lưu output thành file. Khi mở file đã tải về thì đó là 1 file ảnh:vvv </br>
<p>
  <img width="591" height="749" alt="image" src="https://github.com/user-attachments/assets/1e50ae36-1d60-4715-94ac-b8e2204b1789" />
</p>
Nhìn vào ảnh thì ta chú ý đến dòng mã hex trong ảnh. Tiến hành giải đoạn mã đó được flag: picoCTF{forensics_analysis_is_amazing_2561a194}.
