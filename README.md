# Docker

## Doker image

Search image
```sh
docker search apache
```
Dowload image
```sh
docker pull httpd
```
List image
```sh
docker images
```
Get info docker
```sh
docker image inspect httpd
```

Xóa một image:
```sh
docker rmi httpd
```

- thay `httpd` bằng tên hoặc ID image bạn muốn xóa
- Xóa tất cả các image bằng lệnh `docker rmi -f $(docker images -qa)`
- Khi `image` đang được sử dụng để `run` một `container` thì muốn xóa, bạn cần thêm tham số `-f`
        
Đổi lại `tag` của một image:
```sh
docker tag httpd httpd:1.0
```
Build image:
```sh
docker build --tag bulletinboard:1.0 .
```
## Doker container

run container:
docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0

Output image:
- docker save --output [namefile].tar [id image]

192.168.99.100

Stop all container:
docker stop $(docker ps -aq)

Delete all container:
docker rm $(docker ps -aq)

