## Pre Requisite:

SonarQuber Server
Jenkins Server

## Step 1) 
Install "SonarQube Scanner"  plugin in Jenkins as follow.

 
## Step 2) 
- Integrate SonarQube server with Jenkins  as follows.


- Manage Jenkins ---> Configure System ---> SonarQube servers


- Generate the SonarQube server authentication token 
 
- Login into SonarQube with Admin user.
```
http://<<IP Address>>:9000/
Default Credentials:
User: admin
Password: admin
```

- Click on Administration tab.

- Click on Tokens

## Step 3) 
- Execute the SonarQube report for Maven Java Project.

- Select the job , to which we need to run the sonarqube report, click on configure, in Post-build Actions options, 
click on Add post-build action --> Select the SonarQube report for Maven project.
