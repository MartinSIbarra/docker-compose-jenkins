# Jenkins via Docker Compose
A docker compose file to install, in a Docker container, Jenkins and Socat Agent (to automaticaly deploy Docker images) **on linux**.

## Pre-requisites
### Docker
- [How to install Docker](https://docs.docker.com/engine/install/)
### Curl
- [How to install Curl](https://help.ubidots.com/en/articles/2165289-learn-how-to-install-run-curl-on-windows-macosx-linux)

## Setup
Simply run this command:
```
curl https://raw.githubusercontent.com/MartinSIbarra/docker-compose-jenkins/main/install_docker_jenkins | bash
```
This will install Jenkins on you home path and set 2 exec files to start and stop Jenkins.

## Usage

### Running & Sopping Jenkins
Run `jenkins-up` to start Docker containers running Jenkins and Scocat Agent.

Run `jenkins-down` to start Docker containers running Jenkins and Scocat Agent.

### Access Jenkins
Once started you can access Jenkins using this url:
```
http://localhost:41001
```

### First time? You have to unlock Jenkins, don't worry its really easy =D
You will need to provide the initial administrator password. To do this you have to copy/paste the password inside the file /var/jenkins_home/secrets/initialAdminPassword, to get this just run:
```
docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

Now you can start using Jenkis! Enjoy!
