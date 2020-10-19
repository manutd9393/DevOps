# Docker

## Projects
- Hello World - Java, JavaScript and Python
- 2 Microservices - Currency Exchange and Currency Conversion

## Steps
- Building and Pushing Python App Docker Image to Docker Hub
- Building and Pushing Docker Image for Node JavaScript App
- Building and Pushing Docker Image for Java Application
- Running Microservices as Docker Containers
- Using Docker Link to Connect Microservices
- Using Custom Networking to Connect Microservices

## Registry and Repositories

- https://hub.docker.com/repository/docker/manutd9393
- https://hub.docker.com/repository/docker/manutd9393/hello-world-nodejs
- https://hub.docker.com/repository/docker/manutd9393/hello-world-python
- https://hub.docker.com/repository/docker/manutd9393/hello-world-java

# Commands

```
docker --version
docker run -p 5000:5000 manutd9393/hello-world-python:0.0.1.RELEASE
docker run -p 5000:5000 manutd9393/hello-world-java:0.0.1.RELEASE
docker run -p 5000:5000 manutd9393/hello-world-nodejs:0.0.1.RELEASE
docker run -d -p 5000:5000 manutd9393/hello-world-nodejs:0.0.1.RELEASE
docker run -d -p 5001:5000 manutd9393/hello-world-python:0.0.1.RELEASE
docker logs 04e52ff9270f5810eefe1f77222852dc1461c22440d4ecd6228b5c38f09d838e
docker logs c2ba
docker images
docker container ls
docker container ls -a
docker container stop f708b7ee1a8b
docker image history manutd9393/hello-world-java:0.0.1.RELEASE
docker image history 100229ba687e
docker image inspect 100229ba687e
docker image remove mysql
docker image remove manutd9393/hello-world-java:0.0.1.RELEASE
docker container rm 3e657ae9bd16
docker container ls -a
docker container pause 832
docker container unpause 832
docker container stop 832
docker container inspect ff521fa58db3
docker container prune
docker system
docker system df
docker system info
docker system prune -a
docker top 9009722eac4d
docker stats 9009722eac4d
docker container run -p 5000:5000 -d -m 512m manutd9393/hello-world-java:0.0.1.RELEASE
docker container run -p 5000:5000 -d -m 512m --cpu-quota=50000  manutd9393/hello-world-java:0.0.1.RELEASE
docker system events

docker build -t manutd9393/hello-world-java:0.0.1.RELEASE .
docker push manutd9393/hello-world-java:0.0.1.RELEASE

docker build -t manutd9393/hello-world-python:0.0.1.RELEASE .
docker push in28min/hello-world-python:0.0.1.RELEASE

docker build -t manutd9393/hello-world-nodejs:0.0.1.RELEASE .
docker push manutd9393/hello-world-nodejs:0.0.1.RELEASE


docker run -d -p 8000:8000 --name=currency-exchange manutd9393/currency-exchange:0.0.1-RELEASE
docker run -d -p 8100:8100 --name=currency-conversion manutd9393/currency-conversion:0.0.1-RELEASE

docker network ls
docker network inspect bridge

 