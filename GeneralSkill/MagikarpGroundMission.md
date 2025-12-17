Link thử thách: https://play.picoctf.org/practice/challenge/189?difficulty=1&originalEvent=34&page=1
<img width="697" height="726" alt="image" src="https://github.com/user-attachments/assets/d6d6197c-b3d3-4a1a-b061-125f24dc72dc" />
Ta kết nối bằng cách:
ssh ctf-player@wily-courier.picoctf.net -p 54669
Trong đó -p là password

<img width="887" height="192" alt="image" src="https://github.com/user-attachments/assets/e2d17b74-0f0d-4a99-be64-f12c979587c2" />
nhập yes + enter
<img width="845" height="201" alt="image" src="https://github.com/user-attachments/assets/cf5daceb-cce9-42e4-9c21-8b9d59b65744" />
Nhập password đề bài cung cấp

<img width="888" height="509" alt="image" src="https://github.com/user-attachments/assets/92040054-372b-4e08-a167-d43a41f1b84e" />
Kết nối thành công. Sau đó dùng ls để liệt kê các file mình đang có

<img width="416" height="71" alt="image" src="https://github.com/user-attachments/assets/d8a1efbc-cce0-4303-9aac-795ddf9d98ff" />
Ở đây ta thấy có 2 file txt. Tiến hành đọc file cat + tên file
<img width="379" height="61" alt="image" src="https://github.com/user-attachments/assets/e1042dd3-3306-466b-b48e-4292012650fa" />
Đọc file đầu ta được 1/3 cờ.

<img width="479" height="54" alt="image" src="https://github.com/user-attachments/assets/da0b86c0-47d6-4031-850d-773f4494bd78" />
Đọc file thứ 2 ta được 1 gợi ý sử dụng /
Tiến hành cd / đến đến thư mục gốc và ls để xem các mục
<img width="803" height="110" alt="image" src="https://github.com/user-attachments/assets/daf8664f-9f57-4e10-80d2-e3a1f111ff98" />
Ta thấy có thư mục lạ là challenge. Tiến hành truy cập vào thư mục này và ls để liệt kê
<img width="396" height="95" alt="image" src="https://github.com/user-attachments/assets/75beada7-c726-496e-9431-7d4511a17521" />
Ta đấy có file metadata.json
<img width="343" height="35" alt="image" src="https://github.com/user-attachments/assets/b4b09d5a-25b6-4900-a4a5-df0013bd3d24" />
Đọc file này:
Ta có flag: picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}




