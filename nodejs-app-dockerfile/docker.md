# Học image and container

## Tạo image:

- cmd: docker build -t <name>:<tag> .
- cmd tạo nhanh: docker build .

## Kiểm tra container hoạt động

- cmd: docker ps
- cmd: docker ps -a

## Chạy và dừng image:

- docker run <image id>
- docker stop <names>

## Chạy container

- docker start <names>

### Chạy trên port cá nhân ánh xạ vào port container

- docker run -p <port web>:<port container> <image id>:

### Chạy container port chỉ định, tắt terminal, tự rm, tên chỉ định khi dừng container

- cmd: docker run -p <port web>:<port container> -d --rm <image id>
  - -p <port>:<port>: Chỉ định port để chạy và ánh xạ tới port container
  - -d: tắt chế độ chiếm terminal chuyển về chạy ngầm
  - --rm: tự động xóa sau khi stop container
- cmd: docker run -p <port web>:<port container> -d --rm --name <name> <image id>
- cmd: docker run -p <port web>:<port container> -d --rm --name <name> <names>:<tag>
-

## Chế độ attach để xem log khi tương tác với container đang chạy

- cmd: docker attach <names>
- cmd: docker log -f <names>: Xem log từ đầu tới cuối của container

## Xóa container

- cmd: docker rm <names[]>

## Xem và xóa images: nếu image còn nằm trong 1 container nào đó sẽ không thể xóa

- cmd: docker images: xem list image
- cmd: docker rmi <images id[]>

## Đặt tên images

- docker build -t <names>:latest

- vid20

## Đổi tên image:

- cmd: docker tag my-old-image:latest my-new-image:v1.0
