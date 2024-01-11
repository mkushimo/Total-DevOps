# Install Nginx HTTP Server Installation
## Method 3

### Login as root user and execute the below command for install nginx http server.
```
sudo su -
yum -y install wget
wget https://nginx.org/packages/rhel/6Server/x86_64/RPMS/nginx-1.18.0-2.el6.ngx.x86_64.rpm
yum install nginx-1.18.0-2.el6.ngx.x86_64.rpm
systemctl start nginx
systemctl enable nginx
nginx -V
```
