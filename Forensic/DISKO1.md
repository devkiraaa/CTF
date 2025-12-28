Link thử thách: https://play.picoctf.org/practice/challenge/505?difficulty=1&page=1 </br>
Dùng wget để tải file về ta được file disko.dd.gz. Nhìn vào định dạng .gz -> đây là 1 file cần giải nén vì vậy là dùng gunzip để giải nén. ( Tại sao lại dùng gunzip mà không phải unzip thì bởi vì gunzip dùng để giải nén 1 file còn unzip là để giải nén thư mục bên trong có thể chứa nhiều file ) </br>
<p>
  <img width="936" height="165" alt="image" src="https://github.com/user-attachments/assets/4b8ec666-fa26-4e9d-add4-3baae9b5faed" />
</p>
Sau khi giải nén ta được file disko.dd. Bây giờ tiến hành đọc file và tìm kiếm flag. Định dạng cờ là pico{flag} nên ta sẽ tìm kiếm với từ khóa "pico" </br>
<p>
<img width="601" height="238" alt="image" src="https://github.com/user-attachments/assets/dd7c79c6-9afe-4bc4-9329-433f079ad66f" />
</p>
Và ở dòng pico cuối cùng ta đã tìm thấy flag: picoCTF{1t5_ju5t_4_5tr1n9_e3408eef}.
