![image](https://github.com/user-attachments/assets/ee553bb0-e1c2-46e5-a30b-51521c4b4268)


1. Goto Azure Cloud Kubernetes cluster and get the connection configurations
   - kubectl config view --minify --flatten
2. Connect to the kubernetes cluster from EC2 machine
   *   Create namespace for jenkins in Kubernetes cluster
      - kubectl create namespace jenkins
   * Create a service account called jenkins in kubernetes
      - kubectl create sa jenkins -n jenkins
   * Create a token for connecting from Jenkins to Kubernetes that is running on Azure Cloud
      - kubectl create token jenkins -n jenkins --duration=8760h
   * Provide admin permission to Jenkins service account
      - kubectl create rolebinding jenkins-admin-binding --clusterrole=admin --serviceaccount=jenkins:jenkins --namespace=jenkins
3. First create a Kubernetes plugin & connect to Kubernets from Jenkins
   - Go to Manage Jenkins -> Clouds -> New Cloud
      - select name as kubernetes or any other name of your choice
      - kubectl config view --minify --flatten
    
      - ![image](https://github.com/user-attachments/assets/25b71927-ec10-41b4-b259-5d93f28cb375)



2. Then create a Jenkins CD pipeline using below 
   ```
   pipeline {
     agent {
       kubernetes {
         yaml '''
           apiVersion: v1
           kind: Pod
           spec:
             containers:
             - name: maven
               image: maven:alpine
               command:
               - cat
               tty: true
           '''
       }
     }
     stages {
       stage('Run maven') {
         steps {
           container('maven') {
             sh 'mvn -version'
           }
         }
       }
     }
   }
   ```



<!-- [This is commented out.](https://www.youtube.com/watch?v=qcmUy_iFT-A&ab_channel=LearnDevOpsandCloud) -->
