![image](https://github.com/user-attachments/assets/ee553bb0-e1c2-46e5-a30b-51521c4b4268)


1. First create a Kubernetes plugin
2. Connect to the kubernetes cluster
   - kubectl create namespace jenkins
   - kubectl create sa jenkins -n jenkins
   - kubectl create token jenkins -n jenkins --duration=8760h
   - kubectl create rolebinding jenkins-admin-binding --clusterrole=admin --serviceaccount=jenkins:jenkins --namespace=jenkins
   - kubectl config view
2. Go to Manage Jenkins -> Clouds -> New Cloud
   - select name as kubernetes or any other name of your choice
   - kubectl config view


CI pipeline to copy the deploy.yml to the artifact folder using the below pipeline yml
   cd-kubernetes/cd-deploy-to-kubernetes-from-azure-devops
2. Then create a cd using Azure devops
   - First create service connection for Kubernetes
   - Then create the cd pipeline and select the service connection
   - Use apply and select the drop/deploy.yml for the apply

![image](https://github.com/user-attachments/assets/d4425387-adc9-44e7-80da-090ed06bbdff)

<!-- [This is commented out.](https://www.youtube.com/watch?v=qcmUy_iFT-A&ab_channel=LearnDevOpsandCloud) -->
