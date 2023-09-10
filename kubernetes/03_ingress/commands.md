kubectl create namespace ingress-nginx
kubectl apply –f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.2.1/deploy/static/provider/cloud/deploy.yaml
kubectl get all -n ingress-nginx
kubectl get ingress
kubectl get service -n ingress-nginx
kubectl get svc