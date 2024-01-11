# AWS CLI Commands

The AWS CLI is an open-source  tool which we can use to connect to AWS account , 
manage your AWS resources and services from command line interface.

Using AWS CLI we can automate manual AWS tasks through pragmatically.

**Note**: Installing AWS CLI we need to install Python (Python 2 version 2.6.5+ or Python 3 version 3.3+) first. 

- #aws -version: It will display the AWS CLI version which you have installed.

- #aws configure: Using this command we can configure AWS Access Key ID, AWS Secret Access Key, region and output format.
 
An AWS CLI command has the following structure:
```
#aws <command> <subcommand> [options and parameters]
```
---------------------------------------------------------------------------------------------------------------------

## Elastic Cloud Compute (EC2) 

- #aws ec2 describe-instances: It will display all the ec2 instances.
 
- #aws ec2 describe-instances --filters "Name=instance-type, Values=t2.micro”: 
  It will display all the ec2 instances which are having the instance type is t2.micro.

- # aws ec2 describe-instances --filters "Name=tag:Name, Values=RedHat Server": 
  It will display all the ec2 instances which are having the Tag name is "RedHat Server".

- #aws ec2 terminate-instances --instance-ids i-0cf83a9889a47e9e8: It will delete the instance ids which you specified.

See Below output after running above command.
```
i-0cf83a9889a47e9e8 à ec2 instance id.
```

Below screenshot from AWS admin console.

- #aws ec2 describe-instances --filters Name=instance-state-name,Values=stopped --region ap-south-1 --output table : 
  It will display all instances that are currently stopped.
- #aws ec2 describe-instances --filters Name=instance-state-name,Values=stopped --region ap-south-1 --output table : 
  It will display all instances that are currently stopped.
------------------------------------------------------------------------------------------------------

## Identity and access management (IAM) 

- #aws iam list-users --output table: It will display users in a table format.

Here

ARN: It is the Amazon resource name to identify the user

Create Date: It is the user creation date in ISO 8601 date-time format

User ID: It is a unique id of each IAM user

User Name: It is a friendly user name that we specify while creating the IAM user.

- #aws iam create-user --user-name ruthvik: It will create an IAM user.
---------------------------------------------------------------------------------------------------------------------
## Simple Storage Service (S3)

- #aws s3 ls: It will display all the S3 buckets.

---------------------------------------------------------------------------------------------------------------------

Virtual Private Cloud (VPC)
 

---------------------------------------------------------------------------------------------------------------------

