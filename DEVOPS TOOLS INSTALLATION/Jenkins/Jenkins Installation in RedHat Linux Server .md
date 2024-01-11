# Jenkins Installation in RedHat Linux Server
``` 
sudo su -

yum install wget -y

wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
yum install fontconfig java-11-openjdk -y
yum install jenkins -y
systemctl enable jenkins

systemctl start jenkins

systemctl status jenkins
```
