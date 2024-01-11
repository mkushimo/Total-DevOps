# ANSIBLE CHEAT SHEET

## Ansible
- It is an open source engine that automates deployment, orchestration, cloud provisioning and other tools.
- It uses a playbook to describe jobs and uses YAML which is human readable
- It is designed for multi- tier deployment. It is agentless and works by connecting nodes through ssh.

## How does it work?
• Connects nodes and pushes small programs called modules to them and are removed when they are done.

• The management node controls whole execution of the playbook.

• The inventory file provides the list of hosts where the modules need to be run.

• The management node does an ‘ssh’ connection and executes the modules and installs the software.

## Troubleshooting
- Common strategies to debug playbooks are:

  • Debug and register
  
  • Use verbosity (verbosity level)
  
- Playbook issues:

  • Quoting
  
  • Indentation
  
- Some drawbacks are:

  • OS restrictions: is OS dependent so code on one OS will not work for another
  • Once playbook is running, adding of hosts is not possible
  • Error reporting is mediocre.
  
## Environment setup
Types of machines:

  • Control machine : manages other machines
  
  • Remote machine: controlled by other machines
  
Multiple remote systems can be handled by one machine.

  • Remote machine managing is done by ansible by default.
  
  • Ansible doesn’t leave any software running on them. Therefore there is no need of an upgrade when moving to a newer version.
  • Install it through apt, yumpkg, pip, OpenCSW

  • installing it through apt :
```
  $ sudo apt-get update
  $ sudo apt-get install software-properties-common
  $ sudo apt-add-repository ppa: ansible/ansible $ sudo apt-get update
  $ sudo apt-get install ansible
```
  • Run ansible version to make sure it was installed properly.
  
## YAML
• YAML syntax is used to express ansible playbooks

• Key-value pair:

Dictionary is represented in key value pair
```
Ex: james:
name: james john
rollNo: 34
div: B
sex: male
```
• Representing lists:

   • Each element has to be written in a new line with “-” as the prefix
   
   • countries:
   ```
   - America
   - Iceland
   ```
• Lists inside the dictionary:
```
• name: james john
• rollNo: 34
• div: B
• sex: male
• likes:
- english
```
• Boolean terms are also used in YAML

## Advantages of ansible

• It is free and open source.

• Agentless. No master client model.

• System requirements.

• Developed in python.

• Lightweight and quick deployment.

• Ansible uses YAML syntax in config files.

• Large community base.

## Adhoc commands

General syntax of ad-hoc command:
```
Command hostngroup module/options[arguments]
```
Check connectivity of hosts 
```
#ansible <group> -m ping
```
Rebooting hosts 
```
#ansible <group> -a “/bin/reboot”
```
Check host system’s info 
```
#ansible<group> -m steup | less
```
Transfering files
```
#ansible <group> -m copy -a “src=home/ansible dest=/tmo/home”
```
Create new user
```
#ansible<group> -m user -a “name=ansible password= <encrypted password>”
```
Deleting user
```
#ansible<group> -m user -a “name=ansible state- absent”
```
Check if package is installed and update it
```
#ansible<group> -m yum -a “name=httpd state=latest”
```
Check if package is installed and dont update it
```
#ansible<group> -m yum -a “name=httpd state=present”
```
Check if package is s specific version
```
#ansible<group> -m yum -a “name=httpd1.8 state=latest”
```
Check if package is not installed
```
#ansible <group> -m yum -a “name= httpd state= absent
```
Starting a service
```
#ansible<group> -m service -a “name=httpd state=”started”
```
Stopping a service
```
#ansible<group> -m service -a “name=httpd state=”stopped”
```
Restarting a service
```
#ansible<group> -m service -a “name=httpd state=”restarted
```

## Terms
• Service/server- a process that provides service

• Machine - physical machine, Vm or a container

• Target machine - end machine to be configured by ansible

• Task- an action

• Playbook - location where YAMl files are written and executed

## Playbooks

• It is the place where all YAML files are stored and executed. Acts like a to-do list

• YAML- yet another markup language

• A playbook can have more than one plays. Plays map the instructions defined against a particular host

• Typically written in a text editor like notepad or notepad++

Sample playbook/YAML file;
```
name: install and configure DB
hosts: testServer
become: yes
vars: oracle_db_port_value : 1521
tasks:
-name: Install the Oracle DB
yum: <code to install the DB>
-name: Ensure the installed service is enabled
service:
name: <your service name>
```
Tags of YAML:
```
• Name: name of the playbook
• Hosts: specifies the list of hosts. Tasks can be on the same machine or a different one.
• Vars: defines the variables which you can use
• Tasks: it is the list of action that needs to be performed. A task is always linked to a module.
```

## Variables
- Same as using variables in programming languages

    Ex: - hosts : <your hosts>
    
   • tomcat_port : 8080
   
   • Here tomcat_port is assigned to 8080
   
- Keywords used:
   • Block- ansible syntax to execute a block
   
   • Name- name of the block
   
   • Action- the code that is to be executed
   
   • Register- registers the output
   
   • Always- states that below word will be run
   
   • Msg- displays the message
   
- Exception handling:
   • Similar to any other programming language
   
   • Keywords : rescue and always
   
   • The code is written in block
   
   • It goes to the rescue phase and gets executed if the command in the block fails.
   
   • Thereby block is the same as “try block “, catch block is like “ rescue” and always performs the same function as we know.
