# Docker
```
docker build -t eng/cte_k8s:1.4 .
docker tag eng/cte_k8s:1.4 172.16.1.10:8900/eng/cte_k8s:1.4
docker push 172.16.1.10:8900/eng/cte_k8s:1.4
```
# Application
```
docker pull 172.16.1.10:8900/eng/cte_k8s:1.4
docker run -i -t --name tmp  -p 8019:8019 eng/cte_k8s:1.4
```

# k8s
## dep3
```
apiVersion: apps/v1 
kind: Deployment 
metadata:
  name: restapi-deployment
spec:
  replicas: 2
  selector:
    matchLabels:
      app: restapi
  template:
    metadata:
      labels:
        app: restapi
    spec:
      containers:
      - name: restapi
        image: 172.16.1.10:8900/eng/cte_k8s:1.4
        imagePullPolicy: Always
        ports:
        - name: dev
          containerPort: 8019
        resources:
          requests:
            memory: "1000Mi"
            cpu: "500m"
          limits:
            memory: "8000Mi"
            cpu: "2000m"
```


## dep1
```
apiVersion: apps/v1 
kind: Deployment 
metadata:
  name: restapi-deployment
spec:
  replicas: 2
  selector:
    matchLabels:
      app: restapi
  template:
    metadata:
      labels:
        app: restapi
    spec:
      containers:
      - name: restapi
        image: 172.16.1.10:8900/eng/cte_k8s:1.4
        imagePullPolicy: Always
        ports:
        - name: dev
          containerPort: 8019
```
# Servers
```
apiVersion: v1 
kind: Service
metadata:
  name: restapi
  labels:
    app: restapi
spec:
  selector:
    app: restapi
  ports:
  - name: dev
    port: 8080
    nodePort: 30006
    targetPort: dev
  type: NodePort
```
## dep2
```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: restapi
spec:
  replicas: 1
  selector:
    matchLabels:
      app: restapi
  template:
    metadata:
      labels:
        app: restapi
    spec:
      containers:
        name: restapi
        image: 172.16.1.10:8900/eng/cte_k8s:1.4
        imagePullPolicy: Always
        ports:
        - name: dev
          containerPort: 8019
        resources:
          limits:
            cpu: 5000m
            memory: 10000Mi
          requests:
            cpu: 1000m
            memory: 4096Mi
        volumeMounts:
        - mountPath: /data/restapi
          name: restapi-data
      volumes:
      - name: restapi-data
        emptyDir: {}
```
