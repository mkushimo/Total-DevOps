
Install Maven Build Tool in MAC Book / Set Class path for Maven Build Tool in MAC Book
---------------------------------------------------------------------------------------------------------------------

Pre Requisite Software
-----------------------------
Java is the Pre Requisite Software for Maven.

java -version


Install Maven
------------------
Download the Maven Software using below url.
https://maven.apache.org/download.cgi

Set the class path/Environmental Variable
vi ~/.bash_profile

export M2_HOME=/Users/mithunreddy/MithunTechnologies/Softwares/Running/apache-maven-3.6.2

export PATH=$PATH:$M2_HOME/bin

source ~/.bash_profile

Check the Maven version

mvn -version
