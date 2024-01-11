Jenkins Docker Swarm Integration
=========================

1) CI/CD Pipeline Scrit to build and deploy single service in docker swarm


2) CI/CD Pipeline Scrit to build and deploy multiple services using docker stack(Compose File) in docker swarm


Pre Requisite:
==========

1) Docker Swarm Cluster
  
   https://www.youtube.com/watch?v=cuNW5Qwd-D4
  
2)  Setup CI/CD (Jenkins) Server   

=========Install Java, Jenkins, Docker in Ubuntu==============
```
sudo apt update -y

sudo apt install openjdk-8-jdk -y

wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update -y
sudo apt-get install jenkins -y

sudo systemctl status jenkins

sudo curl -fsSL get.docker.com | /bin/bash
```
## Add jenkins user to docker group
```
sudo usermod -aG docker jenkins
```
## Restart jenkins to reflect docker permisions
```
sudo systemctl restart jenkins
```
## Use below commands if you want to switch to jenkins user.
```
sudo -i -u jenkins
sudo su -s /bin/bash jenkins
```
## Plugins Used
```
sshAgent
```
