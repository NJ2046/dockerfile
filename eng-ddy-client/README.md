# Server
```
ssh hello@172.16.1.10
root12300.
```
# Docker
```
docker build -t eng/ddy:1.0 .
docker tag eng/ddy:1.0 172.16.1.10:8900/eng/ddy:1.0
docker push 172.16.1.10:8900/eng/ddy:1.0
```
# Application
docker pull 172.16.1.10:8900/eng/ddy:1.0

