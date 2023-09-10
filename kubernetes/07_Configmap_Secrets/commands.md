kubectl get configmap
kubectl describe cm mongodb-configmap

kubectl get secret
kubectl describe secret mongodb-secret

#### Display environmental variables
kubectl exec <pod-name> env