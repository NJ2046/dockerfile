# Server
```
ssh hello@172.16.1.10
root12300.
```
# Docker
```
docker build -t base/py:3.6 .
docker tag base/py:3.6 172.16.1.10:8900/base/py:3.6
docker push 172.16.1.10:8900/base/py:3.6
```
# Application
docker pull 172.16.1.10:8900/base/py:3.6
