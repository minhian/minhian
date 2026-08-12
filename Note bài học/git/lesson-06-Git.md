**Các thư mục quan trọng cần lưu ý:** 
- Working directory: thư mục project trên máy 
- Staging area: vùng chuẩn bị commit, nơi bạn chọn file nào sẽ được commit tiếp theo
- Local repository: thư mục `git` trên máy, nơi lưu trữ lịch sử commit local 
- Remote repository: Github, Gitlab, Bitbucket, nơi lưu bản online



## PWD  -> Kiểm tra xem đang đứng ở thư mục nào

## ls -> kiểm tra list thư mục to 

- Các bước đẩy code lên remtoe repo 

B1: Khởi tạo git trong folder hiện git init  `git init`
-> Ý nghĩa: làm lần đầu tiên và duy nhất -> sau lệnh này git sẽ tạo ra 1 folder `ẩn` tên là .git 
-> là nơi lưu lịch sử thay đổi của project. Bình thường ko cần mở hoặc sửa ở folder này 

Empty Git repository -> lịch sử đang rỗng vì chúng ta chưa commit lần nào

B2: 
Kiểm tra trạng thái file: `git status`
gitlab -> nhánh master 
github -> nhánh main 

=> Git đã được bật trong folder nhưng chưa tạo mốc lưu đầu tiên 

B3: chạy `git add` 
- Git add . : thêm tất cả các file đang thay đổi trong project 
- Git add + tên file hoặc tên folder -> chỉ add file đó 

