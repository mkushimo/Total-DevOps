# Java Installation in Ubuntu Linux Server 
 
By default, Ubuntu 18.04 includes OpenJDK version 11,which is an open-source variant of the JRE and JDK.

To install this version, first update the package index with below command.
```
#sudo apt update
```

Then execute below commands based on which version you want to install.
```
#apt install default-jre : For Defauly version.
#apt install openjdk-11-jre-headless : For Java 11
#apt install openjdk-8-jre-headless : For Java 8
```

Verify the Java installation with below command.
```
#java -version
```

To install the JDK, execute the following command, which will also install the JRE.
```
#sudo apt install default-jdk
```

Verify that the JDK is installed by checking the version of javac, the Java compiler using below command.
```
#javac -version
```

To Install the Open JDK 8, use the below command.
```
#sudo apt install openjdk-8-jdk
```
