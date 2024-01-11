# Install Scala Build Tool (SBT) in Linux Server

Login as a root user  and execute the below commands
```
sudo su -

curl -L https://www.scala-sbt.org/sbt-rpm.repo > sbt-rpm.repo

sudo mv sbt-rpm.repo /etc/yum.repos.d/

sudo yum install sbt -y

sbt -version
```
