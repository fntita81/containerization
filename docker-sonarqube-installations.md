# Docker Installation

- apt update -y 
- apt install docker.io
- Configure Docker to start on boot: By default, Docker does not start automatically when the system boots up. To enable Docker to start on boot, use the following command:
  - sudo systemctl enable docker

# Running SonarQube Container in Docker 
Now to install sonarqube and to always restart sonarqube after it is exited, use below
- Run the Docker container: Start the Docker container using the docker run command. 
  Make sure to use the --restart always flag to ensure that the container restarts automatically if it crashes or if the EC2 instance reboots. 
  Here's an example command:
  - docker run --restart always -d --name sonarqube -p 9000:9000 sonarqube
