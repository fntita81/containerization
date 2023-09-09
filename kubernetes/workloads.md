#### Get All workloads in kubernetes
kubectl get all -A 

#### Apply deployment
kubectl apply -f sample-deployment.yml

#### Delete deployment
kubectl delete -f sample-deployment.yml

#### Get pods
kubectl get pods

#### Describe pod
kubectl describe pod <pod-name>

#### Delete pod
kubectl delete pod <pod-name>

#### Delete all
kubectl delete -f .


### ReplicaSets

#### Apply ReplicaSet
kubectl apply -f sample-replicaset.yml

#### Delete ReplicaSet
kubectl delete -f sample-replicaset.yml

#### Get replicaset
kubectl get replicaset

#### Describe replicaset
kubectl describe replicaset <Replicaset name>


#### Edit commands
kubectl edit deployment <deploymnent-name>

#### Wait will wait and show the current pods in live
kubectl get pods -w

#### get pods output in wide format
kubectl get pods -o wide


### Service commands
kubectl get service

#### Apply Service
kubectl apply -f <service.yml>

#### Get Service
kubectl get svc
kubectl get service

#### Describe svc
kubectl descrive svc <name-of-service>
kubectl get pods -o wide


#### Get Nodes
kubectl descrive svc <name-of-service>
kubectl get node -o wide