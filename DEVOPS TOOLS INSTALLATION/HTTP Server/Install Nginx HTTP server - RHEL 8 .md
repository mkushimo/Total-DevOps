# Install Nginx HTTP Server Installation
## Method 1

### Login as root user and execute the below command for install nginx http server.
```
sudo su -
yum install nginx -y
```
### Enable the service as follows.
```
systemctl enable nginx.service
```
### Start the HTTP server as follows.
```
systemctl start nginx.service
```
## Method 2

### Login as root user and execute the below command for install nginx http server.
```
sudo su -
dnf install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm

sudo yum install nginx
```
### Enable the service as follows.
```
systemctl enable nginx.service
```
### Start the HTTP server as follows.
```
systemctl start nginx.service
```
### To check the version we will use below command
```
nginx -V
```
## Important Points
```
  nginx.conf file is the configuration file for Nginx HTTP server, which is available in /etc/nginx/ directory.
Logs will be available in /var/log/nginx/ directory.
```
