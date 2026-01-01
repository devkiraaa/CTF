Link thử thách: https://play.picoctf.org/practice/challenge/530?difficulty=1&page=1 </br>
Tiến hành tải file về và mở file lên kiểm tra.</br>
<p>
  <img width="947" height="868" alt="image" src="https://github.com/user-attachments/assets/52457d37-19ff-4125-8833-062bf6331902" />
</p>
Mở file lên thì thấy có nhiều chỗ văn bản đã bị che đi -> Tìm cách hiện thị nhữn 4 
Xem qua văn bản thì mình thấy no flag. Tức là trong đoạn văn bản này không có flag. Bị lừa rồi-.- </br>
Thôi thì thử check thông tin file này xem có gì không.</br>
<p>
  <img width="770" height="311" alt="image" src="https://github.com/user-attachments/assets/48d3f4c2-f695-4783-a223-c4a30e5a8797" />
</p>
Hmm ra vấn đề rồi thấy ở thẻ Author thấy có 1 chuỗi kí tự bị mã base64 -> decode chuỗi xem được gì nhé.</br>
<p>
  <img width="660" height="60" alt="image" src="https://github.com/user-attachments/assets/d7b947f4-e403-4022-b804-ca3a6305447c" />
</p>
Ra flag rồi đó: picoCTF{puzzl3d_m3tadata_f0und!_ee454950}
