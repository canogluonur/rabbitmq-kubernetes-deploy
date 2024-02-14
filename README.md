# rabbitmq-kubernetes-deploy
How Can We Install One RabbitMQ Instance On Kubernetes Cluster

# Step1:
Create new namespace on your cluster.
```
kubectl create ns rabbitmq
```

# Step2:
Create new deployment file like below. We will use the below image that has a management console ui.
```
kubectl apply -f rabbitmq.yaml
```

# Step3:
Create new service yaml file to access the management console and internal communication port.
```
kubectl apply -f rabbitmqsvc.yaml
```

# Step4:
If you want create new ingress to access the management ui.
```
kubectl apply -f ingress.yaml
```

you can enter the following values for the backend to bind.

http://rabbitmq.rabbitmq
username:guest
password:guest
