# Install Tomcat as a Service

## Login as a root user
```
sudo su -

yum install wget unzip -y

cd /opt
wget https://downloads.apache.org/tomcat/tomcat-9/v9.0.44/bin/apache-tomcat-9.0.44.zip
unzip apache-tomcat-9.0.44.zip

chmod u+x /opt/apache-tomcat-9.0.44/bin/*.sh

mv apache-tomcat-9.0.44 tomcat9
```

## Create a system user called tomcat.
```
useradd -r tomcat

cp -r /opt/tomcat9 /usr/local/tomcat9
```

## Create a file called tomcat.service
``` 
vi /etc/systemd/system/tomcat.service


[Unit]
Description=Apache Tomcat Server
After=syslog.target network.target

[Service]
Type=forking

User=tomcat
Group=tomcat

Environment=CATALINA_PID=/usr/local/tomcat9/temp/tomcat.pid
Environment=CATALINA_HOME=/usr/local/tomcat9
Environment=CATALINA_BASE=/usr/local/tomcat9

ExecStart=/usr/local/tomcat9/bin/catalina.sh start
ExecStop=/usr/local/tomcat9/bin/catalina.sh stop

RestartSec=10
Restart=always

[Install]
WantedBy=multi-user.target
```

## Reload the systemd
```
systemctl daemon-reload
```

## Enable the  tomcat service
```
systemctl enable tomcat.service
```

## Start the tomcat service
```
 systemctl start tomcat.service
```

## Check the tomcat service
```
systemctl status tomcat.service

#netstat -tunlap
#ps -fax | grep tomcat


#vi /usr/local/tomcat9/webapps/manager/META-INF/context.xml
```

## Comment the below lines	
```
<!-- 	 
 	 	 	 	<Valve className="org.apache.catalina.valves.RemoteAddrValve"
  allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" />       -->

```
