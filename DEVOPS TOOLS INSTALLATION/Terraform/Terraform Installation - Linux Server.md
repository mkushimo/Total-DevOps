# Terraform Installation

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

## Download the terraform software.
```
#Use https://www.terraform.io/downloads.html to download the terraform software.

wget https://releases.hashicorp.com/terraform/1.3.3/terraform_1.3.3_linux_amd64.zip
```

## Extract the terraform software.
```
unzip terraform_1.3.3_linux_amd64.zip -d /usr/local/bin/
```

## Check the version
```
terraform -v (OR) terraform version
```

## Help
```
terraform -help
```
