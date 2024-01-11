# Steps to Install Node JS in Linux (RedHat and Ubuntu)

## Method -1
----------------
### Login into Linux server and switch to the root user using below command.
```
#sudo su -
```
### Install the NodeJS package as follows.
- In RedHat distribution
```
#yum install nodejs -y   

#yum install npm -y
```

- In Ubuntu distribution
```
#apt-get install nodejs -y

 #apy-get install npm -y
```
------------------------------------------------------------------------------------------------------------------------------------------

## Method -2 (Install the specific version)
----------------------------------------------------

### Login into Linux server and switch to the root user using below command.
```
#sudo su -
#cd /opt
```

### Download the node js specific version of software and extract.
```
yum install wget tar -y ---> RHEL
apt-get install wget tar -y --> Ubuntu

wget https://nodejs.org/dist/v10.15.1/node-v10.15.1-linux-x64.tar.xz
tar -xvf node-v10.15.1-linux-x64.tar.xz
```

### Create a soft link.
```
ln -s /opt/node-v10.15.1-linux-x64/bin/node /usr/bin/node
ln -s /opt/node-v10.15.1-linux-x64/bin/npm /usr/bin/npm
ln -s /opt/node-v10.15.1-linux-x64/bin/npx /usr/bin/npx
```
### Check the version
```
node --version
#node -v
npm --version
#npm -v

#https://github.com/nodejs/help/wiki/Installation
```
