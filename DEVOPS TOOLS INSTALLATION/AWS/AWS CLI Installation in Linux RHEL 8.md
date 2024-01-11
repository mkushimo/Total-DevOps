# AWS CLI Installation

## Login as a root user 
```
sudo su -
yum update -y
```

## Download the AWS CLI software
```
cd /opt
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
```

## Install AWS CLI software
```
 ./aws/install
```

## Check the version using below command
```
aws --version
```

## Configure AWS User
```
aws configure
```
