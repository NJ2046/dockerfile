# Server
```
ssh hello@172.16.1.10
root12300.
```
# Docker
```
docker build -t app/opencv:1.0 .
docker tag app/opencv:1.0 172.16.1.10:8900/app/opencv:1.0
docker push 172.16.1.10:8900/app/opencv:1.0
```
# Application
docker pull 172.16.1.10:8900/app/opencv:1.0
