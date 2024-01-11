Install Gradle Build Tool in MAC Book / Set Class path for Gradle Build Tool in MAC Book
---------------------------------------------------------------------------------------------------------------------

Pre Requisite Software
-----------------------------
Java is the Pre Requisite Software for Gradle.
```
java -version
```

Install Gradle
------------------
Download the Gradle Software using below url.
```
https://services.gradle.org/distributions/
```
Set the class path/Environmental Variable
```
vi ~/.bash_profile

export GRADLE_HOME=/Users/mithunreddy/MithunTechnologies/Softwares/Running/gradle-6.6.1

export PATH=$PATH:$GRADLE_HOME/bin

source ~/.bash_profile
```
Check the Gradle version
```
gradle-version
```


