# Kubernetes Cluster setup in AWS using KOPS

1) Create Ubuntu EC2 instance

2) Install AWSCLI
```
 sudo apt update -y
 sudo curl https://s3.amazonaws.com/aws-cli/awscli-bundle.zip -o awscli-bundle.zip
 sudo apt install unzip python -y
 sudo unzip awscli-bundle.zip
 #sudo apt-get install unzip - if you dont have unzip in your system
 sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws
``` 
3) Install kops on ubuntu instance:
```
     #Install wget if not installed
     sudo apt install wget -y
     sudo wget https://github.com/kubernetes/kops/releases/download/v1.16.1/kops-linux-amd64
     sudo chmod +x kops-linux-amd64
     sudo mv kops-linux-amd64 /usr/local/bin/kops
``` 
4) Install kubectl
```
 sudo curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s 
 https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl

 sudo chmod +x ./kubectl
 sudo mv ./kubectl /usr/local/bin/kubectl
```
5) Create an IAM role from Consloe or CLI with below Policies.
```
    AmazonEC2FullAccess
    AmazonS3FullAccess
    IAMFullAccess
    AmazonVPCFullAccess
```

Then Attach IAM role to ubuntu server from Console Select KOPS Server --> Actions --> Instance Settings --> 
Attach/Replace IAM Role --> Select the role which You Created. --> Save.

6) create an S3 bucket Execute below commond in KOPS Server use unique bucket name if you get bucket name exists error.
```
    aws s3 mb s3://<bucketname>
   
    ex:
    # S3 bucket name should be unique across AWS
    aws s3 mb s3://balajimtbatch18.k8s.local
    
    Expose environment variable:

    # Add env variables in bashrc
    vi .bashrc
   
    # Give Unique Name And S3 Bucket which you created.
    export NAME=balajimtbatch18.k8s.local
    export KOPS_STATE_STORE=s3://balajimtbatch18.k8s.local
 
    source .bashrc
 ```   
7) Create sshkeys before creating cluster
```
    ssh-keygen
``` 
8)Create kubernetes cluster definitions on S3 bucket
```
kops create cluster --zones ap-south-1a --networking weave --master-size t2.medium --master-count 1 --node-size t2.micro --node-count=2 ${NAME}
   
   
    kops create secret --name ${NAME} sshpublickey admin -i ~/.ssh/id_rsa.pub
```
9) Create kubernetes cluser
```
     kops update cluster ${NAME} --yes
```
10) Validate your cluster(KOPS will take some time to create cluster ,Execute below commond after 3 or 4 mins)
```
       kops validate cluster
``` 
11) To list nodes
```
      kubectl get nodes
``` 
To Delete Cluster
```
   kops delete cluster --name=${NAME} --state=${KOPS_STATE_STORE} --yes 
```  
====================================================================================================


IF you wan to SSH to Kubernates Master or Nodes Created by KOPS. You can SSH From KOPS_Server
```
ssh  admin@<IPOrDNS>
it above command  is not working
then execute
ssh -i ~/.ssh/id_rsa admin@<IPOrDNS>
``` 
