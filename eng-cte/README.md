# Server
```
ssh hello@172.16.1.10
root12300.
```
# Docker
```
docker build -t app/ppocr:1.4 .
docker run -i -t --name ppocr -v /home/ai-eng/code/ai-eng-cte:/app -p 8888:5900 -e RESOLUTION=1920x1080 app/ppocr:1.3


ssh login password: Eega2Hufael8
docker tag app/ppocr:1.1 172.16.1.10:8900/eng/cte:1.1
docker push 172.16.1.10:8900/eng/cte:1.1
```
# Application
docker pull 172.16.1.10:8900/eng/cte:1.1

# Test
测试环境不一致导致的结果不一致
docker run -i -t -p 8888:5900  --name ppocr -v /home/ai-eng/code/dev_mysql/ai-eng-cte:/app  172.16.1.10:8900/eng/cte:1.1
ssh login password: Degha4aeL8ah

