# Packer Installation 

## Login as a root user in ec2 instance
```
sudo su -
```

## You will need to upgrade your system and packages
```
yum update -y
```

## Install wget and unzip packages
```
yum install wget unzip vim -y
```

## Go to /opt dir
```
cd /opt
```

## Download the Packer software.
```
https://packer.io/downloads.html 

wget  https://releases.hashicorp.com/packer/1.5.4/packer_1.5.4_linux_amd64.zip
```

## Extract the terraform software.
```
unzip packer_1.5.4_linux_amd64.zip -d /usr/local/bin/
```

## Check the version
```
packer -v (OR) packer --version
```

## Help
```
packer -help
```
