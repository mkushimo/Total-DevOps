# In Ubuntu Server
----------------------
## Method-1
==========

Step 1: Update all Software Repositories using below command.
```
#sudo apt-get update
```
Step 2: Install a Docker using below command
```
#sudo apt install docker.io -y
```
Step 3: Enable and start the docker service as follows.
```
#sudo systemctl enable docker
#sudo systemctl start docker
```
Step 4: Check the  docker version
```
#docker --version
```
You will get permison denied error as regular user dosn't have permisions to execute docker commands, add ubuntu user to docker group.
```
#sudo usermod -aG docker $USER
     or 
#sudo usermod -aG docker ubuntu
```
Exit From Current SSH Terminal & SSH(Login) again .Then execute
```
docker ps
```

To Un Install a docker
-----------------------------
Use below command to un-install docker
```
#apt-get remove docker docker-engine docker.io -y
```
----------------------------------------------------------------------------------------------------------------------------
## Method -2
============
Step 1: Update all Software Repositories using below command.
```
#apt-get update
```

Step 2: Install Docker using below command
```
#curl -fsSL get.docker.com | /bin/bash
```

Step 3: Check all the versions.
```
#apt-cache madison docker-ce
```

Step 4: If we want to install the specific version use the below command.
```
apt-get install docker-ce=<VERSION>
```

Step 5: If you would like to use Docker as a non-root user, you should now consider
adding your user to the "docker" group with something like:
```
#usermod -aG docker  <<YourUser>>
```
============================================================================

# In Amazon Linux
-----------------------
```
sudo yum update -y       
sudo yum install docker -y
sudo service docker start
```
Add Regural user to dockergroup
```
sudo usermod -aG docker  <username>
```
ex:
```
sudo usermod -aG docker ec2-user
```
Once you add user to group exit from the server and login again.
### Get docker information
```
docker info
```
### Install Docker in Linux (Works for most of linux flavors).
```
sudo curl -fsSL get.docker.com | /bin/bash
```
Docker Home Directory/Working Dir:
```
/var/lib/docker
```
----------------------------------------------------------------------
Install Docker on AWS RHEL  (Offcially No Support)
----------------------------------------------------------------------
```
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo dnf install docker-ce-3:18.09.1-3.el7 -y
sudo systemctl enable docker
sudo systemctl start docker

sudo docker info
```
### Check docker is installed or not
```
docker info
```
You will get permison denied error as regular user dosn't have permisions to execute docker commands, add user to docker group.
```
sudo usermod -aG docker $USER
or
sudo usermod -aG docker ec2-user
```
Exit From Current SSH Terminal & SSH(Login) again .Then execute
```
docker ps
```
