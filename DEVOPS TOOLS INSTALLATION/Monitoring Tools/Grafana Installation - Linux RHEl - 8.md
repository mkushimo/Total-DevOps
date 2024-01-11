Grafana Installation

#Login as a root user
sudo su -

#Create file called grafana.repo in /etc/yum.repos.d directory and add the below content.
vi /etc/yum.repos.d/grafana.repo

[grafana]
name=grafana
baseurl=https://packages.grafana.com/oss/rpm
repo_gpgcheck=1
enabled=1
gpgcheck=1
gpgkey=https://packages.grafana.com/gpg.key
sslverify=1
sslcacert=/etc/pki/tls/certs/ca-bundle.crt

#Install the grafana.
yum install grafana -y

#Enable the grafana-server service.
systemctl daemon-reload

systemctl enable grafana-server

#Start the grafana-server service.
systemctl start grafana-server

#Check  the grafana-server service status.
service grafana-server status


Troubleshooting
---------------------
Unable to access Grafana URL?
----------------------------------------
https:<<IP Address>>:3000/

Deafult Credentails
User Name: admin
Password:  admin

a)make sure port 3000 is opened in security groups in AWS ec2 instance.
