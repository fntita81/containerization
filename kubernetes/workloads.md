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