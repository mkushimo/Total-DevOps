ELK  Stack Installation

#Login as a root user
sudo su -

Install Elastic Search
---------------------------

#rpm --import https://artifacts.elastic.co/GPG-KEY-elasticsearch

Create a file called elasticsearch.repo in the /etc/yum.repos.d/ directory for RedHat based distributions and Added below lines

#vi /etc/yum.repos.d/elasticsearch.repo

[elasticsearch]
name=Elasticsearch repository for 7.x packages
baseurl=https://artifacts.elastic.co/packages/7.x/yum
gpgcheck=1
gpgkey=https://artifacts.elastic.co/GPG-KEY-elasticsearch
enabled=0
autorefresh=1
type=rpm-md

Install the Elasticsearch package

#yum install --enablerepo=elasticsearch elasticsearch -y

To configure Elasticsearch to start automatically when the system boots up, run the following commands:

#/bin/systemctl daemon-reload

#/bin/systemctl enable elasticsearch.service

Start the Elasticsearch service as follows.

#systemctl start elasticsearch.service


Directory Structure for Elastic Search

https://www.elastic.co/guide/en/elasticsearch/reference/current/rpm.html


Kibana
-----

rpm --import https://artifacts.elastic.co/GPG-KEY-elasticsearch

vi /etc/yum.repos.d/kibana.repo


[kibana-7.x]
name=Kibana repository for 7.x packages
baseurl=https://artifacts.elastic.co/packages/7.x/yum
gpgcheck=1
gpgkey=https://artifacts.elastic.co/GPG-KEY-elasticsearch
enabled=1
autorefresh=1
type=rpm-md



yum install kibana -y


systemctl enable kibana.service

https://www.elastic.co/guide/en/kibana/7.8/rpm.html#rpm-repo


Logstash
---------
rpm --import https://artifacts.elastic.co/GPG-KEY-elasticsearch

vi /etc/yum.repos.d/logstash.repo

[logstash-7.x]
name=Elastic repository for 7.x packages
baseurl=https://artifacts.elastic.co/packages/7.x/yum
gpgcheck=1
gpgkey=https://artifacts.elastic.co/GPG-KEY-elasticsearch
enabled=1
autorefresh=1
type=rpm-md


 yum install logstash -y


systemctl enable logstash.service

systemctl start logstash.service


