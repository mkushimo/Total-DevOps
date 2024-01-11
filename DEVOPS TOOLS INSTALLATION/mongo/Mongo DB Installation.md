Mongo DB Installation 
#Login as a root user
sudo su -

#Configure the package management system (yum).
#Create a file /etc/yum.repos.d/mongodb-org-4.2.repo

vi /etc/yum.repos.d/mongodb-enterprise-4.2.repo

#add below lines in /etc/yum.repos.d/mongodb-org-4.2.repo file

[mongodb-enterprise-4.2]
name=MongoDB Enterprise Repository
baseurl=https://repo.mongodb.com/yum/redhat/$releasever/mongodb-enterprise/4.2/$basearch/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.2.asc

#Install the mongodb
yum install -y mongodb-enterprise

#Enable the mongod service
systemctl enable mongod
#Start  the mongod service
systemctl start mongod
#Check the mongo db version
mongo --version

#Connect to mongo db
mongo
#Create a user

use admin
 
db.createUser(
  {
    user: "mithuntechnologies",
    pwd: "passw0rd",
    roles: [ { role: "userAdminAnyDatabase", db: "admin" } ]
  }
)

#Enable authentication

vi /etc/mongod.conf

security:
    authorization: "enabled"
   
#Restart the mongod service as follows.

service mongod restart

# Connect to Mongo DB from any client
mongo mongod:IPAddress:27017


