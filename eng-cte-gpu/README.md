# Server
```
ssh hello@172.16.1.10
root12300.
```
# Docker
```
docker build -t eng/cte_gpu:1.0 .
docker tag eng/cte_gpu:1.0 172.16.1.10:8900/eng/cte_gpu:1.0
docker push 172.16.1.10:8900/eng/cte_gpu:1.0
```
# Application
```
docker pull 172.16.1.10:8900/eng/cte:1.1
docker run -i -t --name cte_gpu -v /root/nhj/ddy_demonstration/ai-eng-cte/project:/app -p 8021:8020 eng/cte_gpu:1.0
```

