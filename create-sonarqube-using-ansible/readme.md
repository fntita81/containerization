Step 1 :
1. Setup inventory file using below command 
    - vi /opt/ansible/ansible_hosts
    - Then either copy the ini file or the yml format content provided in the inventories folder
2. Then run the playbook to install sonarqube in the intended ec2 instance "your_ec2_instance"
    - ansible-playbook sonarqube-playbook.yml

