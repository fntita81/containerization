# Docker Installation

- Command 1 : apt update -y
  - To get latest updated packages  
- Command 2 : apt install docker.io
  - Install docker that is needed for running SonarQube
- Configure Docker to start on boot: By default, Docker does not start automatically when the system boots up. To enable Docker to start on boot, use the following command:
  - Command 3 : 
  - sudo systemctl enable docker
    - Enable Docker

# Running SonarQube Container in Docker 
Now to install sonarqube and to always restart sonarqube after it is exited, use below
- Run the Docker container: Start the Docker container using the docker run command. 
  Make sure to use the --restart always flag to ensure that the container restarts automatically if it crashes or if the EC2 instance reboots. 
  Here's an example command:
  - Command 4 : docker run --restart always -d --name sonarqube -p 9000:9000 sonarqube
