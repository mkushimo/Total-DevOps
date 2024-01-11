# JENKINS CHEATSHEET

Jenkins is a software which allows you to do continuous integration on your application/software lifecycle. 
It gets installed on the server where the central build will take place. Now, let's understand it's workflow.

## MANAGEMENT
### Configure system:

- can be used to manage paths to various tools used in builds.

- Jenkins dynamically adds the config fields after the plugins are installed.

### Manage Plugins:
- plugins can be removed, updated and installed by manage plugin screen.

### System info:
- list all the current java properties and system environment variables.

- system log - view Jenkins log in real time.

- script console - lets you run groovy scripts on the server.

- manage nodes - configure the number of builds you want.

- shutdown - click prepare to shutdown link to prevent any new builds from being started. After all current builds are finished, 
  Jenkins will shutdown cleanly.
  
## UNIT TESTING
Testing unit in Jenkins:

Step 1: go to the dashboard and choose an existing project and click configure.

Step 2: browse to add a build step and invoke Ant.

Step 3: click on advanced.

Step 4: in the build file section, enter the location of build.xml.

Step 5: add post build option and click Publish Junit test result.

Step 6: ensure the report is in the folder of the project workspace. The "*xml" basically tells 
Jenkins to pick up the result xml files which are produced by the running of the Junit test cases. Click save after done.

Step 7: click on build, and check logs to see if successful or not with applications.

## AUTOMATED TESTING
step 1: go to plugins and choose selenium plugins and click to install.

step 2: go to configure system and select on selenium jar and save.

step 3: go to the dashboard and select the config option for the project at hand.

step 4: click on add build step and choose SeleniumHQ htmlsuite Run".

step 5: add the required details and click on save, execute and build. The test is executed, and a report is built.

## AUTOMATED DEPLOYMENT
- head to the manage plugins and install the repective plugins.

- it takes the war ear file and deploys that to the running remote application build.

- go to build and congigure and click on 'deploy to war/ear to container'

- in the war container section, save details about the destination server and click save.

## BACKUP PLUGIN
- to tweak backup settings via setup.

- to backup Jenkins config.

- to restore config from a previous backup.

- alternatively, you can use SCM(sync congig plugin) or ThinBackup for global and job configuration.

## NOTIFICATIONS
- Jenkins comes with a feature to add email notifications to the build project.

- go to manage Jenkins x configure system. in the email notification space, enter the require STMP server and use email suffixes.

- configure the recipients so that they would receive notification about brokenn or unstable builds.

- notification plugins such as Tikai knowledge allows job status  notification for JSON and XML formtas.

- options:
  
  - Format: either Json or XML types
  
  - Protocol: TCP, UDP or HTTP
  
  - Event: job event that triggers the notification.
  
  - URL: dstination to send notifications to.
  
  - Timeout: default timeout 30ms

## MANAGE PLUGINS
- to uninstall plugins, go to manage plugins and click on the installed tab and click on uninstall for the plugin.

- in case of need to install an older version for the plugin, download from the site and click on upload option to do it manually.

## CODE ANALYSIS
They provide utilities for static code analysis. Some tools are Checkstyle, FindBugs, PMD etc.

Provides details like:
- Total warning in a job.

- showing of new and fixed warning of a build.

- trend reports showing warnings of a build.

- warnings per module, package or category.

- detailed reports of found warnings.

## SERVER MAINTENANCE
### COMMANDS IN JENKINS: (URLS)
- http://localhost:8080/jenkins/exit - shutdown Jenkins

- http://localhost:8080/jenkins/restart - restart Jenkins

- http://localhost:8080/jenkins/reload - to reload

### to backup Jenkins Home:
- go to configure system in manage Jenkins.

- select a partition that has to most free space.

- perform automated clean-up options to avoid this.

## BUILD PIPELINE
- first go to manage plugin and install b8uild pipeline plugin

- to see a build pipeline, click the (+) on the dashboard

- enter any name and click on the view. Choose build pipeline view.

- accept the default settings and add the name of the project.

- a view of entire pipeline with statuses will be visible.

## REMOTE TESTING
Selenium tests can be run on remote slave machines via master slave and selenium suite plugin installation.

Step 1: go to master jenkins server and manage nodes.

Step 2: click on configure for the slave machine.

Step 3: put the launch method as 'Launch slave agent via Java Web start'

Step 4: open a browser instance of the master Jenkin on the slave machine, then manage nodes and select the DXMBMEM30.

Step 5: scroll down and select the lauch option and hit run.

Step 6: configure tests to run on the slave

Step 7: make sure the selenium part of the job is configured. Make sure that the sample.html file and the selenium-server.jar/
