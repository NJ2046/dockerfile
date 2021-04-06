# Docker
```
docker build -t centos/py:3.6 .
docker tag centos/py:3.6 172.16.1.10:8900/centos/py:3.6
docker push 172.16.1.10:8900/centos/py:3.6
```
# Application
docker pull 172.16.1.10:8900/centos/py:3.6
