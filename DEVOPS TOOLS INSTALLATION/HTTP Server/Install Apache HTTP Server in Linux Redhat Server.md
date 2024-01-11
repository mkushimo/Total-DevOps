# Install Apache HTTP Server Installation 
## Login as root user and execute the below command for install http server.
```
yum install httpd -y
```
## Enable the service as follows.
```
systemctl enable httpd.service
```
## Start the HTTP server as follows.
```
systemctl start httpd.service
```
### Important Points
```
 httpd.conf file is the configuration file for Apache HTTP server, which is available in /etc/httpd/conf directory.
Logs will be available in /etc/httpd/logs directory.
```
