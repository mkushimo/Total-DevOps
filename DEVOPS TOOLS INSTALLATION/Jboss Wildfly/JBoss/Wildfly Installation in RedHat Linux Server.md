# Installation in RedHat Linux Server
Login As a root user
```
sudo su -

cd /opt

wget https://github.com/wildfly/wildfly/releases/download/25.0.1.Final/wildfly-preview-25.0.1.Final.zip

unzip wildfly-preview-25.0.1.Final.zip

cd /opt/wildfly-<<Version>>.Final/standalone/configuration/

cd /opt/wildfly-preview-25.0.1.Final/standalone/configuration/
```
Find and replace 127.0.0.1 with your Private IP address in standalone.xml like below
```
vim /opt/wildfly-13.0.0.Final/standalone/configuration/standalone.xml
<wsdl-host>${jboss.bind.address:172.31.24.62}</wsdl-host>
<inet-address value="${jboss.bind.address.management:172.31.24.62}"/>
<inet-address value="${jboss.bind.address:172.31.24.62}"/>

sh /opt/wildfly-preview-25.0.1.Final/bin/add-user.sh
sh /opt/wildfly-preview-25.0.1.Final/bin/standalone.sh
```
