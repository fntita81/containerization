kubectl apply -f mysql-cm.yml
kubectl apply -f mysql-secret.yml
kubectl apply -f mysql-svc.yml
kubectl apply -f mysql-sc.yml
kubectl apply -f mysql-sts.yml


kubectl get svc
kubectl get pods -o wide