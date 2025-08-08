# Feedback

## Build image feedback

- cmd: docker build -t feedback-node .

## Chạy container

- cmd: docker run feedback-node<:latest>

## Cache

- Khi run container không có --rm thì khi dừng container mà k xóa. dữ liệu của container sẽ không bị mất

# Giải pháp lưu trữ tránh tường hợp xóa container mất vùng chứa?

## Volumes - Giúp lưu trữ ngoài container

### Build docker:

- cmd: docker build -t <names>:volumes .

### Lấy volume name

- cmd: docker start ... -v ....

# Docker ignore

- loại trừ những file hoặc thư mục không cần thiết khỏi quá trình docker build.

# ENV

- Ẩn các giá trị nhạy cảm khi chạy

## Build

- cmd: docker build -t names:env .

## Chạy với env

- cmd: docker run -d --rm --name -p 3000:PORT --env-file ./.env

## Build ARG

- cmd: docker build -t names:dev --build-agr DEFAULT_PORT=8000
