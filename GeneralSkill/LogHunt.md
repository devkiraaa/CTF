Link thử thách: https://play.picoctf.org/practice/challenge/527?difficulty=1&page=1
Sử dụng máy ảo và tải file ảnh về: wget + link ảnh
<img width="937" height="289" alt="image" src="https://github.com/user-attachments/assets/1da3ca2f-bcde-4ab4-91a1-0fdd66ba5078" />
Ta sẽ được 1 file ảnh có tên server.log.1
Đọc file và tìm kiếm từ pico
<img width="446" height="202" alt="image" src="https://github.com/user-attachments/assets/39547aac-b351-44de-b9dc-ca796e62ce82" />
Ta thấy được 1 phần của flag. Và cụm từ trước flag là INFOR FLAGPART: -> Ta sẽ đọc lại file và tìm kiếm với từ khóa INFOR FLAGPART để tìm được các phần còn lại của flag
<img width="451" height="477" alt="image" src="https://github.com/user-attachments/assets/53595997-698b-468d-9a70-15f1534f7e37" />
Có nhiều phần bị lặp lại nên ta chọn ra và ghép lại với nhau ta có flag: picoCTF{us3_y0urlinux_sk1lls_cedfa5fb}
