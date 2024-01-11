# MySQL Database Installation  in Ubuntu 

### Login as a root user
```
sudo su -
```
### Update the system packages.
```
apt-get update -y
```
### Check mysql packges in the server.
```
apt-cache search mysql
```

### Install the mysql packages.
```
apt-get install mysql-server mysql-client  -y
```

### Check the status of mysql service
```
systemctl status mysql
```

### Enable the mysql service
```
systemctl enable mysql
```

### Check the which version of MySQL server installed using below command.
```
mysqld --version
```

### Check the which version of client utility installed using below command.
```
mysqladmin -V
```

### MySQL database server configuration file is availabe in /etc/mysql/mysql.conf.d directory.
```
See the configurations..
less /etc/mysql/mysql.conf.d/mysqld.cnf

mysql_secure_installation
```

### Connect to mysql server
```
mysql -u root -p
```

### Check the MySQL server version
```
SELECT VERSION();

SHOW VARIABLES LIKE "%version%";
```

### Using below command we can see how long the MySQL server has been running.
```
STATUS;
(OR)
mysqladmin version
```

### To Display database.
```
show databases;
```
