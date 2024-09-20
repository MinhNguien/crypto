## Tạo repository (repo)

git init
=> nhánh chính: master

### git init -b main

=> Tạo repo local vs nhánh chính có tên main

## git remote add origin + <url repo>

=> Liên kết repo local vs repo remote

## Ko đưa thư mực node_modules lên repo remote

=> Node_modueles chiếm dung lượng rất lớn
=> Node_modules có thể cài lại thông qua câu lệnh : npm i

## file .gitignore quy định những thư mục hay file ko đc phép đẩy lên repo remote

=> .gitignore nằm ở ngoài thư mực root

### git status

=> kiểm tra sự thay đổi của cái file trong dự án

### git add

### git add . => dung để thêm tất cả các file ở trong thư mục hiện tạu vào trong staging

### git add -A => dùng để thêm tất cả các file ở trong dự án vào trong staging

# git add <đường dẫn file> => chỉ thêm file cụ thể vào trong staging

=> Thêm file vào trong staging

### woring directory (file màu đỏ)

### staging (file màu xanh)

=> lúc này file sẵn sàng để đưa lên repo remote

### config git (chi chạy duy nhất 1 lần)

### git config --global user.name "name"

### git config --global user.email "abc@gmail"

### git commit -m "message"

=> dùng để gắn message vào trong những file đang ở staging được phép đưa lên repo remote
=> mỗi commit có một mã sha (id)

### git log

=> dùng để kiểm tra lịch sử commit

### git push -u origin <tên nhánh>

=> đưa code lên repo remote
=> từ lần push code thúe 2 : git push

### Đưa file từ staging về lại working

    git reset

    git restore -S . (đưa tất cả các file ở staging về working)

    git restore -S <url file> (chỉ đưa duy nhất file về working)

### git checkout <url file>

=> 1. Đưa 1 file được chỉnh sửa về trạng thái trước đó

### git checkout -b <tên nhánh >

=> tương đương với 2 lệnh git branch và git switch

### git checkout <tên nhánh >

=> tương đương vs lệnh git switch
=> dùng để chuyển qua <tên nhánh>

### branch

// dev => Kiểm thử QA và Dev (dev)

// staging => QA Kiểm thử 1 lần (staging)

// production => end user (main/release)

git branch < tên nhánh>
=> tạo ra 1 nhánh mới
=> nhánh mới sẽ chứa toàn bộ code của nhánh đang đứng

git branch -a or git branch
=> liệt kê tất cả các branch đang có trong repo

git switch <tên nhánh>
=> chuyển qua nhánh <tên nhánh>

### git pull

=> pull code ở repo remote về local

<!-- fix loi fast-forward only -->

git pull --no-ff

### git clone <url repo>

=> Dùng để clone source code của 1 repo bất kì
