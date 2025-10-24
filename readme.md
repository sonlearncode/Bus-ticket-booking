# các bước chạy run application trên docker

Bước 1: build từng server
cd MainServer
mvn clean package -DskipTests

cd ../SubServer
mvn clean package -DskipTests

** Lưu ý: nếu có sự thay đổi phải build lại **

Bước 2:
cd ..
docker-compose up --build -d

## để dừng server

docker-compose down

## để đọc logs

docker-compose logs main-server

# set up loadballance Nginx trên windows

# 1. Tải Nginx từ trang chính:

https://nginx.org/en/download.html

# 2. Giải nén và cấu hình lại nginx.conf

Bố cục file lên page đọc docs

# 3. Lưu lại, mở CMD quyền admin

Mở tại vị trí sau: ..\nginx-1.x.x\nginx-1.x.x

# 4. Run lệnh

nginx

# 5. Kiểm tra config

Chạy lệnh: nginx -t

Ra kết quả như sau là ok:
nginx: the configuration file D:\tools\myApp\nginx-1.26.3\nginx-1.26.3/conf/nginx.conf syntax is ok
nginx: configuration file D:\tools\myApp\nginx-1.26.3\nginx-1.26.3/conf/nginx.conf test is successful

(Khởi động lại nginx -s reload)
(Dừng NGINX nginx -s stop)
