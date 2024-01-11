# Install Python in Linux Server

## Login as a root user
````
sudo su -

wget https://www.apache.org/dyn/closer.lua/spark/spark-3.1.2/spark-3.1.2-bin-hadoop3.2.tgz

tar -zxvf spark-3.1.2-bin-hadoop3.2.tgz

ln -s /opt/spark-3.1.2-bin-hadoop3.2 /opt/spark

useradd spark

chown -R spark:spark /opt/spark*

vi /etc/systemd/system/spark-master.service

[Unit]
Description=Apache Spark Master
After=network.target

[Service]
Type=forking
User=spark
Group=spark
ExecStart=/opt/spark/sbin/start-master.sh
ExecStop=/opt/spark/sbin/stop-master.sh

[Install]
WantedBy=multi-user.target


vi /etc/systemd/system/spark-slave.service.service

[Unit]
Description=Apache Spark Slave
After=network.target

[Service]
Type=forking
User=spark
Group=spark
ExecStart=/opt/spark/sbin/start-slave.sh spark://rhel8lab.linuxconfig.org:7077
ExecStop=/opt/spark/sbin/stop-slave.sh

[Install]
WantedBy=multi-user.target


#systemctl daemon-reload

#systemctl start spark-master.service

#systemctl status spark-master.service

http://IpAddress:8080
```
