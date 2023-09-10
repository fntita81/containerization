kubectl get nodes
kubectl get all
kubectl get pv
kubectl get pvc
kubectl get pods


kubectl apply -f ./pvc.yml
kubectl apply -f .
kubectl get pvc
kubectl get pv

kubectl edit pv <pv-name>

kubectl get deployment
kubectl describe deployment my-deployment

kubectl get pods
kubectl describe pod <pod-name>

kubectl get deploy
kubectl get pv
kubectl get pvc

#### delete a deployment
kubectl delete deploy my-deployment
kubectl get pv
kubectl get pvc
kubectl get pods

#### if we delete a pvc, then pv will be deleted
kubectl delete pvc my-pvc