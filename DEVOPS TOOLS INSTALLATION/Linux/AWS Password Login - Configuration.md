
Enable a password login instead of pem file when logging into EC2 Instance using SSH
================================================================

Procedure to Enable the password login
---------------------------------------------------
Step 1) First login into ec2 instance with pem file, then switch to root user.
ssh -i "mithuntechnologies.pem" ec2-user@ec2-52-66-196-244.ap-south-1.compute.amazonaws.com

sudo su - (OR) sudo -i

Step 2) Set a password for ec2-user as follows.
       
passwd ec2-user
       
Step 3) Update the PasswordAuthentication parameter in the /etc/ssh/sshd_config file as follows.
       
vi /etc/ssh/sshd_config
       
PasswordAuthentication yes

Step 4) Restart the sshd service as follows.

service sshd restart
