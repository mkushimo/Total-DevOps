# Steps to create password less ssh between two AWS EC2 instances

## Pre Requisites

  2 Linux Servers
     Redhat Linux Server - A
     IP:       13.233.128.180
     User:     ec2-user
     Password: ********
   
     Redhat Linux Server - B
     IP:       13.127.64.6
     User:     ec2-user
     Password: ********

## Step  1

Generate the ssh key using below command in Redhat Linux Server - A
```
ssh-keygey
~/.ssh/
id_rsa
id_rsa.pub
```

## Step 2
Copy the public key from Redhat Linux Server - A to Redhat Linux Server - B as follows.
```
ssh-copy-id ec-user@Redhat Linux Server - B HostName/IP Address
```

## Step 3
Test the configurations as follows.
```
ssh ec2-user@Redhat Linux Server - B HostName/IP Address
```
It should not ask the password and It will successfully connected to Redhat Linux Server - B from Redhat Linux Server - A
