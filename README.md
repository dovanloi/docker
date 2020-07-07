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
docker build --tag app:1.0 .
```
## Doker container

```
docker run -it --publish 8000:8081 --detach --name bb app:1.0  
```

Lệnh xóa tất cả các container trên host: 
``` docker rm -f $(docker ps -aq) ```
