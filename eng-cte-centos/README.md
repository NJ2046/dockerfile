# Server
```
ssh hello@172.16.1.10
root12300.
```
# Docker
```
docker build -t app/ppocr:1.4 .
```
# Application
docker pull 172.16.1.10:8900/eng/cte:1.1

# Test
测试环境不一致导致的结果不一致
docker run -i -t -p 8888:5900  --name ppocr -v /home/ai-eng/code/dev_mysql/ai-eng-cte:/app  172.16.1.10:8900/eng/cte:1.1
ssh login password: Degha4aeL8ah


# starlette
```
docker build -t cte_starlette .


docker run -d -m 10000M  --cpuset-cpus="22,23" --name cte_s2  -p 8049:8049 -e BIND="0.0.0.0:8049" cte_starlette
```

# flash
```
docker build -t cte_fun .

docker run -d --name mycontainer -p 8019:8019 cte_fun
```
