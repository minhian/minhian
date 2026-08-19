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


B4: Tạo commit đầu tiên: 
`git commit -m "nội dung mô tả commit"` 

B5: đặt tên nhánh chính là main (vì github đặt tên nhánh chính là main) 
`git branch -m main`  (m= modify)

B6: gắn folder này với remote repository trên git 
-> nối git ở local với remote repo để chia sẻ code
`git remote add origin + đường link remote repo`
-> sau push (đẩy code) lên repo được gắn link
ví dụ: git remote add origin https://github.com/meomew-auto/JS_TS_BASIC

B7: push đẩy code 
lần đầu chưa đẩy code -> ta phải thiết lập upstream cho branch local hiện tại với remote
`git push -u origin main`
-u = upstream -> lần đầu tiên phải upstream để cho lần sau github ghi nhớ, ko cần gọi lại nữa
origin là tên ngắn của repo github mà mình đã gắn link vào 


Có nhiều môi trường
Dev: main -> nhánh này là nhánh chính chạy ổn định -> khi làm việc mình phải tạo ra một nhánh khác để làm việc để không ảnh hưởng đến nhánh chính đang sử dụng -> sau khi code ổn định ở nhánh phụ, sau đó mới merge code vào nhánh chính để bổ sung thêm tính năng 
UAT: main -> 

Cách đặt tên commit: 
- khi project có nhiều commit -> cần lịch sử để biết
 + sửa gì 
 + ai sửa
 + thêm tính năng gì

 ví dụ: 
 add login test 
 fix login validation 
 update git lesson 
 remove locator 

 type + nội dung thay đổi 
 ví dụ: 
 docs: update git lesson 
 feat: add product search flow
 test: add login test 
 fix: correct bug ... 

HEAD -> main: là vị trí đang đứng
mình sẽ cần phải update code liên tục với nhánh main 
`git fetch`
`git pull`
để kéo code mới nhất từ nhánh main về

Tóm quần lại: 
Flow: `Git pull -> Git add . -> git commit -m "abc" -> git push`

`git branch` kiểm tra đang ở nhánh nào 

cách đặt tên nhánh, ko dấu, ko có khoảng trắng
docs/git-lesson
feat/product-search
fix/ 
test/

trước khi tạo nhánh mới nên quay về main
lý do: nhánh mới sẽ được tạo ra trên nhánh hiện tại, nên phải quay về main để tạo nhánh từ main ra
Flow: quay về main -> pull code mới nhất -> tạo nhánh từ đó

`git checkout main` -> chuyển sang nhánh main
-> `git checkout `-> chuyển qua một nhánh nào đó 

`git merge` + tên branch cần merge vào main

