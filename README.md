# docker
Docker basic
## Docker image
Build image:
docker build --tag bulletinboard:1.0 .

run container:
 docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0

192.168.99.100

Stop all container:
docker stop $(docker ps -aq)

Delete all container:
docker rm $(docker ps -aq)

