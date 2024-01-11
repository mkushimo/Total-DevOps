Prometheus  Installation

#Login as a root user
sudo su -
yum install wget -y

Create a new User called prometheus.

useradd -m -s /bin/bash prometheus

Switch to the prometheus user and download the Prometheus software.

su - prometheus
wget https://github.com/prometheus/prometheus/releases/download/v2.19.2/prometheus-2.19.2.linux-amd64.tar.gz

Extract the prometheus-2.19.2.linux-amd64.tar.gz file and rename the directory to 'prometheus'.

tar -xvf prometheus-2.19.2.linux-amd64.tar.gz
mv prometheus-2.19.2.linux-amd64/ prometheus/

Create a new 'data' directory that will be used as a 'tsdb' storage.

mkdir -p ~/prometheus/data

Configure Prometheus As a Systemd Service

Create new service file 'prometheus.service' using vi editor in  '/etc/systemd/system/' directory

vi /etc/systemd/system/prometheus.service

Paste the prometheus service configuration below.

[Unit]
Description=Prometheus Server
Documentation=https://prometheus.io/docs/introduction/overview/
After=network-online.target

[Service]
User=prometheus
Restart=on-failure

#Change this line if you download the
#Prometheus on different path user
ExecStart=/home/prometheus/prometheus/prometheus \
  --config.file=/home/prometheus/prometheus/prometheus.yml \
  --storage.tsdb.path=/home/prometheus/prometheus/data

[Install]
WantedBy=multi-user.target


Now reload the systemd system using the systemctl command below.

 systemctl daemon-reload

Start the prometheus service and enable it to launch everytime at system startup.

systemctl enable prometheus
sudo systemctl start prometheus


systemctl status prometheus

systemctl status prometheus

http://10.5.5.15:9090/graph
