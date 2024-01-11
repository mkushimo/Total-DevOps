# Java Installation  in RHEL

## Login as a root user
```
sudo su -
```

## Change dir to /opt
```
cd /opt
yum install wget -y
wget -c --header "Cookie: oraclelicense=accept-securebackup-cookie" 
http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.rpm
yum install jdk-8u131-linux-x64.rpm -y
java -version
```
