Step 1 :
- Create Azure Kubernetes Cluster
Create Service Connection

Step 2 :

Create Service connection

**Option 1:**
If you are using Azure Cloud Kubernetes Cluster and Azure DevOps combination, then below configuration is applicable with Authentication method as "Azure subscription"
<img width="476" alt="image" src="https://github.com/user-attachments/assets/880a0a3f-6f76-4875-a3f5-82d725ab853c">

**Option 2:**
If you are using AWS Cloud Kubernetes and Azure DevOps combination, then below configuration is applicable with Authentication method as "Kube Config"
kubectl config view --minify --flatten


Step 3: 

Create a CI pipeline for build, test, build an image (version 0.*) and push an image (version 0.*) 
The CI pipeline below does 2 things
1. Build and Push the image
2. copy the deploy.yml to the Azure artifact folder by copying to drop folder. The deploy.yml cannot be pushed to Docker Hub and also it should be accessible for the CD pipeline

<img width="1661" alt="image" src="https://github.com/user-attachments/assets/f7c5d4da-c71f-45f8-9e5f-5ba8b7764993">
<img width="1459" alt="image" src="https://github.com/user-attachments/assets/3f28afdf-41ca-434b-a569-7852edd7038a">

<img width="1483" alt="image" src="https://github.com/user-attachments/assets/b7d6a2dd-2216-4e33-b946-7305bdb17406">

<img width="1492" alt="image" src="https://github.com/user-attachments/assets/fb6d3231-5e34-40e7-999d-bcb20dc3e4da">

<img width="1429" alt="image" src="https://github.com/user-attachments/assets/a8fb4ebe-0c11-4fb2-a9e0-02bc3c3992f0">

Step 4:
Create a Release pipeline as below
   - Use apply and select the drop/deploy.yml for the apply

<img width="1656" alt="image" src="https://github.com/user-attachments/assets/5fdb6074-700c-4627-8f03-3401f710a49e">

<img width="1633" alt="image" src="https://github.com/user-attachments/assets/1f0c4b29-f038-40c8-9571-ec7c1a07c740">

<img width="1447" alt="image" src="https://github.com/user-attachments/assets/803f34ab-ffe6-456a-8db8-7ee4b85c081f">

<img width="1479" alt="image" src="https://github.com/user-attachments/assets/b599129c-a427-477f-b306-e007ccddda5a">


![image](https://github.com/user-attachments/assets/58a733d0-e887-4ab8-a694-031669fc2fc2)


<!-- https://www.youtube.com/watch?v=UEyWTeL7PX8&t=741s&ab_channel=DevOpsShack -->
