Install Maven Build Tool in Linux Server/ Set Class path for Maven Build Tool in Linux Server
-------------------------------------------------------------------------------------------------------------------------

Pre Requisite Software
-----------------------------
Java (JDK) is the Pre - Requisite Software for Maven.

javac -version

Install Maven
------------------
Step1) Login as a root user and change the directory to /opt/

sudo su -
cd /opt/
yum install wget unzip -y

Step2) Download the Maven Software

wgethttps://dlcdn.apache.org/maven/maven-3/3.9.0/binaries/apache-maven-3.9.0-bin.zip
unzip apache-maven-3.9.0-bin.zip

Step3) Set the class path/Environmental Variable

For Specific User
----------------------
vi ~/.bash_profile

export M2_HOME=/opt/apache-maven-3.9.0

export PATH=$PATH:$M2_HOME/bin

source ~/.bash_profile

For All Users
---------------------- 
vi /etc/profile
export M2_HOME=/opt/apache-maven-3.9.0
export PATH=$PATH:$M2_HOME/bin

source /etc/profile

Step4) Check the Maven version

mvn -version
