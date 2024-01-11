# DevOps Interview Questions  

## GIT

1. What is the difference between GIT and SVN?
2. Advantages of using GIT?
3. What is STAGING area and INDEX in GIT?
4. What is the difference between GIT PUSH and COMMIT? When they are used?
5. What is GIT STASH?
6. How do you create a branch in GIT?
7. How do you merge code from branch to master in GIT?
8. How do you confirm if GIT branch has merged into master?
9. What is HEAD in GIT? How many HEADS you can create in GIT?
10. What does "git config" do?
11. Learn about all the commands in GIT. Interviewer may ask indirectly about how can u acheive one scenario. You should be able to tell him the command to use.
12. What is the purpose of branching in GIT? What is the common branching pattern in GIT?
13. How can u resolve conflict in GIT? Interviewer may also ask you to explain one scenario how you resolved conflicts in GIT in your current project.
 ----------------------------------------------------------------------------------------------------------------------------------------
 
## SVN

1. Difference between GIT and SVN repository?
2. What all things we can store in SVN repository?
3. Difference between "svn import", "svn add" and "svn commit" ?
4. What is the difference between "svn export", "svn checkout" ?
5. What is the difference between "svn update and "svn commit" ?
6. What is the command to see what is inside the svn repository?
7. How can you revert to previous version in SVN?
8. Best prctices of SVN
9. How can u resolve conflict in SVN? Interviewer may also ask you to explain one scenario how you resolved conflicts in SVN in your current project.
10. How can see the difference between the local version and repository version of files in SVN?
----------------------------------------------------------------------------------------------------------------------------------------
 
## Maven


1. Explain Maven Build Lifecycles?
2. What is convention over configuration. How does maven use it?
3. What are the phases of Build Life cycle and Clean life cycle? What happens in each phase?
4. Explain maven dependency
5. When does maven use external dependency?
6. What is Build profile and what are the different types of Build Profile?
7. What are the different types of Maven Repositories? (or) they may ask difference between types of maven repositories
8. What is the sequence in which maven search for dependencies?
9. What is the difference between snapshot and version in maven?
10. What is system dependency and transitive dependency in Maven?
11. How profiles are specified in maven?
12. Explain about all the dependency scopes in Maven
----------------------------------------------------------------------------------------------------------------------------------------

 
## Docker 

1) difference between add and copy ?
2) difference between CMD and entry point ?
3) ADD . .
4) what is docker file ?
5) how to check how many containers are running ?
6) docker logging driver ?
7) what is difference between bridge network and custom bridge network?
8) difference between overlay network and host network ?
9) what is port forwarding in docker what is the use of it ?
10) how to login/enter to a container?
11) what is docker system prune and docker image prune?
12) how many types of volumes are there in Docker? (Local and network)
13) How to check image vulnerabilty ?
----------------------------------------------------------------------------------------------------------------------------------------


## Kubernetes

1) what is taint and toleration
2) node affinity an pod affinity
3) how to check the logs of a pod or deployment?
4) how to check how many pods are running
5) what are deployment strategy used in your project
6) what is init container
7) what is statefullset
8) what is ingress
9) difference between headfull and headless service
10) difference between secret and configmap
11) what is livenessprobe and readynesspeobe
12) how to access other pods in a cluster
13) what is a pod
14) how you will make sure that the database should start first and then application
15) Types of storage class used in your project
16) difference between statefullset and stateless
17) describe kubernetes architecture
18) difference between PV and pvc
19) 2 containers are running inside a pod if one container goes down then will it affect other running container
20) Update the password in secret without restarting the pod or deployment ,is it possible ?
21) how to rollback the deployment?
22) what is the reason for pod eviction?
22) pod is in pending state ,what are the possible reasons?
23) how you will make sure that in rolling update strategy 2 pods are always available?
24) crashloopbackoff, what are the possible reasons?
25) why you are using 3 master node in production?
26) how you will make sure that pod should be running on a specific node?
27) how to check what are the activities performed by the container while creating the pod
28) how to get the ip of a pod ?
29) which network plugin you are using?
30) how you are monitoring the kubernetes cluster and the containers
31) Job should be terminated after 40 seconds ? ActiveDeadLineSeconds: 40
 
----------------------------------------------------------------------------------------------------------------------------------------


## Terraform
 
1) What is statefile and what is the use of it ?
2) where you are keeping the statefile ?
3) how to declare a varible ?
4) what is the difference between provisioner and provider?
5) how pass a value from one resource block to another ?
6) how to reuse a module?
7) what is the differnece between Terrform init and terraform apply?
8) how to validate the the terraform file ?
9) what terraform plan does?
10) how to create 10 ec2 instance using the same script ? ( count= 10)
11) By mistake if you downgrade the instance from t2.large to t2.micro ,then what will happen when you run the terraform script?
----------------------------------------------------------------------------------------------------------------------------------------


## AWS

1) What is EFS ?
2) how to configure S3 with SDN?
3) s3 lifecycle policy
4) static website hosting using s3
5) Describe your project architecture ?
6) What is private subnet and public subnet?
7) what is NAT gateway ? other way , No one can access the database server from internet but from database server we can download the patch?
8) can we mount s3 on ec2 instance?
9) can we make s3 bootable?
10) what are routing policy in rout53?
12) how to take snapshots of a rds database in every 3 hours?
13) how to get the public ips of all ec2 instance under a single user account ?
14) user's are complaing they are not able to access the server ,what is approach to fix this ?
15) differnece between security group and NACL?


----------------------------------------------------------------------------------------------------------------------------------------


- What is difference between VMWare & Docker?
- Explain docker structure?
- What is the use of ant & maven?
- What is pom.xml?
- what is ant and maven file name?
- Difference between build.xml and pom.xml?
- what is war, ear? & Difference between them?
- How to integrate sonarqube with jenkins?
- How to restart jenkins?
- how to install plugin?
- If a plugin is not available then how to install that plugin u want ? 15. Have you used nexus ? what is the work of nexus?
 
----------------------------------------------------------------------------------------------------------------------------------------

 
1.If I wanna delete particular repository in branch how to delete?

2.what are the different roles we can give to developers in GIT?

3.I am committing a code in a particular branch, how the pipeline will go to that particular branch and execute CICD. How we do that in Pipeline?

4. my linux server is fluctuating. how to check why it is fluctuating? Reason behind that? how to fix that?

5.what is the standard permission of a file when it is getting created?

6. Special Permission of linux

7.What you mean by sudo

8.I have a directory and it has 3 folders each has some amount of data I wanna check how much size its using everyday through a shell script using crontab

9.Can you write shell script to monitor the process and give report in mail

10. what you mean by high availability

11. If you gonna build docker image how you are going to build?

12. I wanna deploy an application using tomcat how you are going to dockerize?

13. ADD and COPY command Difference

14. CMD and ENTRYPOINT difference

15. how to push image to private repository

16. What you mean by Kubernetes?

17. Explain architecture of Kubernetes? use of each components

18. what you mean by container?

19. Tell me about Ctrl manager, Scheduler

20. What is the use of ETCD?

21. Difference Services which you used in Kubernetes?

22. What is the LoadBalancer?

23. Use of Kubelet?

24. What you mean by rolling update ? what are different types of rolling updates in Kubernetes

25. How you gonna achieve zero down time while deploying?

26. Strategies in Rolling Update?

27. What is Readiness and Liveness?
----------------------------------------------------------------------------------------------------------------------------------------

 
## GIT 
 
- What is difference bw GIT and SVN
- What is GIT Reset and Revert?
- What is alternate way for merging code instead of GIT Merge?
- Difference Bw GIT Merge and Rebase
- How you will merge code from Development Branch to QA Branch?
- What are the branching Strategy you use in your project?
- How you will give access to developers in a repository?
- Do you create particular Branch for each Developer?
 
## MAVEN
 
- What is the life cycle of Maven?
- Explain its goal
- Where do you configure?
- What are the repository available in Maven?
- Difference bw Maven and Jenkins ?
- Difference bw install and deploy?
 
## NEXUS

- Do you have access to nexus server?
- why do you need access to it?

## SONARQUBE

- What is port number of Sonarqube?
- What is the use of Sonarqube?
- How do you define code coverage in sonarqube?

## JENKINS

- what is jenkins?
- what are the plugins you have used ?
- If you wanna migrate jenkins to new upgraded server, how to do it?
- what are plugin used for sonarqube and Code Coverage?
- Pre requisites for Jenkins?
- How to do add nodes to master?
- Can I use different OS to nodes and master?
- What are different ways to create jobs in jenkins?
- What are different types of pipeline scripts?
- what is the diff bw scripted and Declarative pipeline?
- what are 3 important stages in pipeline?
- what are the diff stages of pipeline?
- what is the last stage in pipeline?
- How to select jenkinsfile which is in repository?
- How to configure nexus username and password ?
- How to configure kubernetes and Docker in pipeline script?
- Where i can configure tools in Jenkins GUI?
- How you will check whether build is success or not?
- Can you configure if a job completed successfully, it should trigger another one?If yes, how to do?
- How to stop particular stage in a pipeline being executed?
- what are the different ways to automate jobs?
- Any plugin to migrate jobs from one server to another?
- How many master and slave machine your project has?
- what is master and slave architecture?

## DOCKER

- What is Containerization?
- Diff bw containerization vs virtualization?
- Commands in Dockerfile?
- Diff bw RUN and CMD and ENTRYPOINT?
- how to create a container which should only have one file[without Tomcat]?
- Why Docker Compose?
- How to check Docker logs and where it get stored?
- What is ImagePullbackoff?
- diff bw docker run and docker pull
- Diff Networks in Docker?

## KUBERNETES

- What you mean by Kubernetes?
- Explain architecture of Kubernetes? use of each components
- what you mean by container/pod?
- Tell me about Ctrl manager, Scheduler
- What is the use of ETCD?
- Difference Services which you used in Kubernetes?
- What is the LoadBalancer?
- Use of Kubelet?
- What you mean by rolling update ? what are different types of rolling updates in Kubernetes
- Strategies in Rolling Update?
- What is Readiness and Liveness?
- What is ConfigMap and Secret? where do u use them?
- Diff types of LoadBalancer?
- Explain Ingress?
- What is HELM and what is the use of it?
- what are the strategies available in k8s?
- What is Blue-Green?
- How to check logs of pod?
- Different ways to configure K8s?
- How many master and slaves you have?
- What if one master goes down? what is the impact?
- If a end User access an application how the request goes to the particular pod?
- How to configure service and an object?
- What is RC and why we go for RC?
- What is RBAC?

## OTHERS
- What is code as infrastructure?
- difference ways to deploy an application in a VM ?  Ans: we can ssh to each machine or we can use was Ansible
- Have u used Route table?
- Can you get alert from Prometheus?
- If you are getting alert as kubelet is down? then what is the issue?
- By seeing subnet IP address can you determine whether an IP belongs to that VPC or not?
- what are different volumes in EC2?
- How to configure AWS CLI?
----------------------------------------------------------------------------------------------------------------------------------------
