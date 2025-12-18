Link thử thách: https://play.picoctf.org/practice/challenge/524?difficulty=1&page=1
<img width="933" height="259" alt="image" src="https://github.com/user-attachments/assets/49bccbdd-a8ef-4ad1-a629-49ed71b8ba8f" />
Tiến hành tải file -> ta có file img.jpg
<img width="516" height="423" alt="image" src="https://github.com/user-attachments/assets/65820192-a3f2-44ba-b373-540025413a0f" />
Ta đọc các thông tin của file
Ở mục comment ta thấy có 1 đoạn kí tự được mã hóa base64 -> Ta thử decode chúng
<img width="427" height="53" alt="image" src="https://github.com/user-attachments/assets/a350a87d-d38d-41d3-8a6b-2aa38d87989b" />
steghide:cEF6endvcmQ= -> dùng stghide với password được mã hóa base64
Tiếp tục decode password
<img width="306" height="36" alt="image" src="https://github.com/user-attachments/assets/b6739e77-3abb-42c7-8d83-7a13cb395938" />
Bây giờ ta sẽ tiến hành giải nén file ảnh với password đã có
<img width="319" height="78" alt="image" src="https://github.com/user-attachments/assets/519c73ad-b7b8-4db6-ad50-a548a048cd35" />
Tiến hành đọc file flag.txt
<img width="292" height="66" alt="image" src="https://github.com/user-attachments/assets/7ecf307b-2ec4-4935-87dc-d948ca3e618d" />
Ta có flag: picoCTF{h1dd3n_1n_1m4g3_67479645}
