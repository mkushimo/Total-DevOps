# JFrog Artifactory OSS Installation
## Pre Requisites

Java is the pre requisite for installing JFrog Artifactory .

Follow below url for installing Java.
```
https://mithuntechnologies-devops.blogspot.com/search/label/Java
```
## Login as a root user
```
sudo su -
cd /opt
yum install tar wget -y
```
## Download the JFrog artifactory software 

Use below to select the version
```
https://jfrog.com/download-legacy/  --> PRO Editions

https://jfrog.com/open-source/#artifactory --> OSS Editions

wget https://bintray.com/jfrog/artifactory-rpms/rpm -O bintray-jfrog-artifactory-oss-rpms.repo

sudo mv  bintray-jfrog-artifactory-oss-rpms.repo /etc/yum.repos.d/
```
## Install the JFrog artifactory software
```
yum install jfrog-artifactory-oss
```
## Enable the artifactory services
```
systemctl enable artifactory
```
## Start the artifactory service
```
systemctl start artifactory
```
## Check the artifactory service status
```
systemctl status artifactory
```
## Access the JFrog Artifactory server from Laptop/Desktop browser.
``` 
http://IPAddess/Hostname:8081/
```
## Default Credentials
```
User Name: admin
Password: password
```
Troubleshooting
---------------------
artifactory service is not starting?
a)check java is installed or not using java -version command.

Unable to access JFrog Artifactory URL?
----------------------------------------------------
- make sure port 8081 is opened in security groups in AWS ec2 instance.
