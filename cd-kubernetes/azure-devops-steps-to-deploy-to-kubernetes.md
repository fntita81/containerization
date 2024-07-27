1. First create a CI pipeline to copy the deploy.yml to the artifact folder using the below pipeline yml
   cd-kubernetes/cd-deploy-to-kubernetes-from-azure-devops
2. Then create a cd using Azure devops
   - First create service connection for Kubernetes
   - Then create the cd pipeline and select the service connection
   - Use apply and select the drop/deploy.yml for the apply

![image](https://github.com/user-attachments/assets/58a733d0-e887-4ab8-a694-031669fc2fc2)


<!-- https://www.youtube.com/watch?v=UEyWTeL7PX8&t=741s&ab_channel=DevOpsShack -->
