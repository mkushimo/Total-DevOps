# Linux Basics

## Linux Command Line Syntax

Command-Name {Options} {Inputs}

Options:
```
  - <Single Character>
  -- <Single Word>
 ``` 
Standard option to all the commands is --help
  
Example:
uname --help
ls –l –d /opt

• Unlike windows Linux Commands are case-sensitive.

• You can get the help of any command by using man pages.

• Linux is more command line friendly than UI tools.

## Linux Commands – System Information
• To check whether the machine is a 32bit or 64bit we can use the following command.
• uname –i
   • On the output if it shows i386/i586/i686 then it is 32bit
   • On the output if it shows as x86_64 then it is 64bit.

## Linux Operating System - Architecture

Users
 ||
Software Utilities => Operating System
 ||
Linux / Kernel
 ||
Hardware

- Linux is not an operating system and it is a code which drives the hardware.
- Vendors like RedHat pull the Linux code and embed that with software's and ships that as operating system.

## Linux Commands – Operating & Hardware Info
• To check the vendor of operating system.
```
cat /etc/*release
```
• To check the CPU information.
```
cat /proc/cpuinfo
```
• To check the memory information.
```
cat /proc/meminfo
```
• To check the disk information
```
fdisk -l
```
• To become more professional way of using command line you need to
have lot of hands on on CLI shortcuts. Following is one of the reference link for such shortcuts.
```
https://github.com/fliptheweb/bash-shortcuts-cheat-sheet
```
• You can pick any link of your choice in google to get shortcuts

## Command Prompts
- Going forward we may need to perform some admin activities as well. In such cases we need to understand the prompt for executing commands..

- Command prompt can help in determining whether you are a root (admin) user or a normal user.
```
   $ - Prompt denotes you are normal user
   
   # - Prompt denotes you are root user
```
   
- In companies we usually login with our account as normal user, but we can gain the root access to the system using sudo command
which we will discuss that further.

## Linux Commands – Listing files and Directories
• In the Linux basic commands we prefer to start with ls command.

• ls command can fetch the files and directories in the current
  directory.
  
• ls -> Get list of files and directories, but it may not show hidden files.

• Hidden files in Linux were created with .filename.

• ls –A -> Get list of hidden files and directories.

• ls –l -> Get list of files with long format, usually shows properties of a file.

• ls –Al -> We can combine multiple options as well, but depends on command.

## Linux Commands – Creating files.
• We can create files in Linux in multiple ways/commands. As a basic we always use touch command to create a file.

• Syntax: touch file-name -> Creates an empty file.

• Example: touch sample notes.txt lambda.py

• touch command can create multiple files as shown.

• In Linux we don’t have any file extensions. Extensions we may use it for our understanding.

## Linux Commands – Remove files
• To remove files we have rm command, Also we can use unlink command which performs the same action, yet we prefer mostly to use rm command.

• Syntax: rm file-name

• Example: rm sample

• Some times it may ask for a prompt (yes/no) to remove the files which may require to parse –f option to not prompt it.

## Linux Commands – Copy files
• To copy a file we have cp command. Alternatively we have rsync command as well but mostly we prefer to use cp command in general.

• Syntax: cp source-file destination-file

• Example: cp file1.txt file2.txt

• If the destination file already exists then it will overwrite the file and in few cases it may warn you to overwrite the file or not.

## Linux Commands – Renaming files
• To rename a file we use mv command

• Syntax: mv source-file destination-file

• Example: mv file1.txt file2.txt

• If the destination file already exists then it will overwrite the file and in few cases it may warn you to overwrite the file or not.

• mv command intention is to move the file from one location to another location and yet it is also mainly used to rename the files.

## Linux Commands – Present Working Directory
• To Check in which directory you are in then pwd command can help you on that.

• It is always important to observe the directory you are in before executing the command, because in some cases if you try to execute
some command and which you lead to loss of data if you execute commands in wrong location.

## Linux Commands – Change Directory
• To change your working directory from one location to another we use cd command.

• Syntax: cd <directory>
  
• Example : cd /bin <- You will switch to /bin directory.
                       
• cd <- Simple cd command will take you to user home directory.
  
• cd - <- A hyphen symbol after cd command can take you to previous working directory.
          
• cd .. <- Double dot denotes parent directory and it can take you to parent directory of existing directory.
  
## Linux Basics– Single dot(.) and double dot(..)
• Dots in Linux denote the present working directory. You can use that in the commands which we have used so far.
  
• cp /opt/file1.txt .
  
• Here dot denotes to copy the file in this location without specifying any filename or path.
  
• Double dot denotes the parent directory which we can understand that after discussing about directories and their management.
  
## Linux Commands – Create Directory
• To create a directory you can use mkdir command.
  
• Syntax: mkdir <directory>
  
• Example : mkdir demo <- It will create an directory.
                          
• mkdir –p demo/new/item1 <- -p Option will be used to create a directory recursively even if the parent directory is missing.
  
• mkdir dir1 dir2 - <- Command mkdir can create multiple directories also at the same time.
                       
## Linux Commands – Remove Directory
• Removing directory commands needed to be picked based on requirement.
                       
• To remove empty directories we use rmdir command.
                       
• To remove directories recursively we use rm command
                       
• Syntax: rmdir <empty-directory> or rm –r <directory>
  
• rmdir demo <- It removes the directory only if demo directory is empty
                
• rm –r dir1 dir2 - <- Command rm –r can delete multiple directories also at the same time and it will remove all the files recursively.
  
## Linux Commands – Copy Directory
• Copying directories can be done with cp command.
  
• While copying the directories we need to mention –r option to enable that we are copying directories.
  
• Syntax: cp –r dir1 dir2 <- It copies dir1 to dir2 and all the contents of dir1 will be copied to dir2 as well.
                             
• If dir2 already exists then dir1 will be copied inside dir2
                             
## Linux Commands – Moving Directory
• Moving directories or renaming directories can be done with mv command.
                             
• Syntax: mv source destination <- Depends on the situation it will rename or move.
  
• If destination does not exists then it renames the directory.
  
• If destination exists:
  
  • Destination is a file - Then that is a invalid operation.
  
  • Destination is a directory – Then the source will be moved into destination directory.                             

## Linux Commands – Concatenate a file
• In view the complete content of a file then we will concatenate (cat) the file.
  
• Syntax: cat <file-name> -> It shows complete content of a file
  
• For demo purpose I would copy one system file and demonstrate using it.
  
• $ cp /etc/passwd .
  
• $ cat passwd <- Shows the complete content of a file
                  
• $ cat –n passwd <- Shows the content with line numbers added on output.
  
• $ tac passwd <- It will print the lines in reverse order mean last line in first and first line at last.
                  
• In most cases you don’t need the complete content, Hence we need filters.
                  
## Linux Commands – head command filter
• In most cases we may not the complete file content, So in those cases we need some filters to get only content which is needed.
                  
• Command head will get the top 10 lines and it can be changed as per our need.
                  
• Syntax: head <file-name> <- Prints top 10 lines by default
                              
• head –n 5 passwd <- Print top 5 lines  
  
## Linux Commands – tail command filter
• Head command can give the top lines however tail command will print lines of a file from ending
  
• Command tail will get the last 10 lines and it can be changed as per our need.
  
• Syntax: tail<file-name> <- Prints last 10 lines by default
                             
• tail –n 5 passwd <- Print last 5 lines
  
• tail –f file-name <- -f option is used to follow the file and all the contents which are getting added to the file will be displayed on the screen.
                       
• To come out of tail –f you can press CTRL +C on terminal.
                       
## Linux Commands – grep command filter
• In case if we need only the lines which are having a particular word or a string then grep command is the right command. It searches a 
   word and prints only those lines.
                       
• Syntax: grep word file-name
                       
• Example : grep root passwd <- It fethes all the lines having a word root in passwd file.  
  
## Linux Commands – awk command filter
• Some cases the content need to be filtered based on columns. Such cases we can approach either cut command or awk command. 
  I would prefer to use awk command over cut command.
  
• Syntax: awk –F ‘Delimiter’ ‘{print $Column-Number}’ file

• Example:
  
   • awk –F : ‘{print $1}’ passwd
  
   • awk -F : ‘{print $1,$2}’ passwd
  
• $NF is used to print nth field which is last one in case if you don’t know how many number of fields exist in that file.
  
## Linux Commands – File Editors
• RedHat Linux has so many utilities that edits the file and its content. Utilities like vi, vim, gedit, nano are widely used and that
depends on user choice. But vi is widely used and vim is a enhanced version of vi. So will discuss about vim in our sessions.
  
• Editor vim is not available by default in CentOS 7 operating system, So lets install it before using it.
  
• $ sudo yum install vim -y  
  
## VI Editor – ESC MODE
```  
• / -> Search a word .. Ex: /root
• yy -> Yank (Copy) a single line
• nyy -> Yank n lines
• p / np -> Paste copied line / Paste n times
• dd / ndd -> Cut\Delete a line / n lines
• u –> Undo Changes like CTRL+z in windows
```
  
## VI Editor – COLON MODE
```
• :/word -> Search a word
• :w -> Save the changes
• :q -> Come out of editor after saving changes
• :q! -> Come out of editor without saving changes
• :wq -> Save and Quit
• :%s/word1/word2/. -> Search word1 and replace with word2 in the file
   • %s/word1/word2/g -> Considers global replacement on line
   • %s/word1/word2/i -> Considers case insensitive of word1 while searching and replaces with word2
```
  
## VI Editor – INSERT MODE
• Insert mode is to add / remove content like your normal editor in windows.
  
## Linux Commands – Finding Files :: find command
• Most of the times you login to a system where you don’t know where the files which you are looking for and definitely need to find those
files to do your job.
  
• Finding the files can be done with multiple utilities, yet find command is a very powerful utility available in most of Linux distributions.
  
• Syntax: find <location-to-find> <search-criteria>
  
• Examples:
  
  • find / -name sample.conf -> Find all the system and get file named sample.conf
  
  • find /boot –type d -> Find all directories in /boot and list
  
  • find / -iname “*.conf” –type f -> Find in all system and get all the file names ending with .conf.
  
## Linux Commands – Command line Browser
• Most of the time you need to browse URLs and fetch that content over the command line. Some times we need some partial
information of that URL else we need complete information of that URL.
  
• Command curl is available to browse the content over the command line
  
• Syntax: curl URL
  
• Some cases that URL might be some downloadable software and in those cases
  
• Syntax: curl URL –o file-name-to-save-download
  
## Linux Commands – Downloading files
• Most of the times we just need to download the software of different tools which we work on. To just download the software we can use wget command.
  
• Command wget just downloads the file in the location which you are in, Else you can provide a custom location as well.
  
• Syntax: wget <URL>. -> Downloads in current directory

• Syntax: wget –O /opt/<file-name <URL> -> Downloads the file in given path and name  
                                    
## Linux Commands – Extract tar archives
• Most of the times download the software from internet of different tools which we use. And some of those tools are archives which are
compressed either in .zip or .tar format. In order to extract tar files then we use tar command and for .zip files it is unzip command.
  
• Command tar can be used for both extraction and creation of archives.
  
• To extract the tar archives we use –x option.
  
• Syntax: tar –xf <file>.tar.gz -> Extracts the file
  
• Usually we find tar files with compression applied are .gz and .bz2.
Command tar can understand what compression was applied and it extracts automatically with out even specifying any option. 
  
## Linux Commands – Pipes
• Pipes are used to send one command output as input to another command.
  
• Pipes converts STDOUT as STDIN, And commands those which accepts STDIN can only be used with pipe.
  
• For an example rm command will not accept STDIN, Hence cannot be used with pipes.  

  
## Linux Commands – Process Management
• Every command we execute in Linux will create a process and every process will get an associated ID which we generally call it as PID and
it is unique in the OS which is taken care by Kernel.
  
• As part of our job we will manage such processes run inside server. In order to manage those process we need the information about the
process. Command ps can help us in getting required/all process running inside the OS.
  
  • ps -> List the process running in current session
  
  • ps –u -> List process running by the user you logged in.
  
  • ps –e -> Get all process running inside OS
  
  • ps –ef -> All process listed out with more detailed way. 
  
We do need to manage these process, Some cases we need to stop/kill them.
  
• To kill any process under Linux OS can use kill command.
• Command kill will be used to kill the process with PID as input provided.
  
• In general we use two type of killing a process by using a signal number 15 and 9, 15 is default signal and we no need to specify in particular.
  
  • kill PID -> Kill the process of given PID with 15 sig
  
  • kill -9 PID -> Kill the process of given PID with 9 signal.
• 15 signal is graceful kill and where as 9 is forceful kill of a process.
  
## Linux Commands – Administration
• In RedHat/CentOS Linux, All admin activities cannot be performed by normal user. We need to be a root user to perform any activities.
  
• To perform those admin activities we use sudo command to gain the root access and perform those admin commands.
  
• To any admin command we can prefix sudo command to gain root privilege.
  
• As we are using cloud based servers we usually login with normal user like centos and such default users will have complete sudo access by default.
  
• In companies we usually will have individual accounts and we can perform the admin activities which are allowed using sudo access.
  
### Linux Commands – Administration
• In RedHat/CentOS Linux, All admin activities cannot be performed by normal user. We need to be a root user to perform any activities.
  
• To perform those admin activities we use sudo command to gain the root access and perform those admin commands.
  
• To any admin command we can prefix sudo command to gain root privilege.
  
• As we are using cloud based servers we usually login with normal user like centos and such default users will have complete sudo access by default.
  
• In companies we usually will have individual accounts and we can perform the admin activities which are allowed using sudo access.
  
• To add a user to multiple groups.
  
• usermod –a –G bin raju
  
• To set a password to the user (Clouds will not use password by default)
  
• passwd raju
  
• You can switch user from one user to another user using.
  
• su - raju
  
• To again another user with out password using sudo
  
• sudo su - raju

### Linux Administration – SUDO configuration
• Sudo configuration allows users to execute sudo commands which are defined here. To add a user to multiple groups.
  
• sudo visudo
  
### Linux Administration – Package Management
• RedHat Linux uses rpm for packaging. Such packages can be downloaded and installed using yum command which uses rpm command in backend.
  
• YUM has capability to download and install the packages from different sources which are defined under /etc/yum.repos.d/*.repo
  
• sudo yum list / sudo yum list all
  
• sudo yum list installed
  
• sudo yum list available
  
• sudo yum install httpd –y
  
• sudo yum remove httpd –y
  
• sudo yum update httpd –y 
  
  
### Linux Administration – Service Management
• RedHat Linux 7 uses systemctl command to manage the services, Earlier till 6 version we use to use service command.
  
 To list all services which are active.
```
 sudo systemctl list-units -t service
```
 To start/stop/restart a service.
```
• sudo systemctl start httpd
• sudo systemctl stop httpd
• sudo systemctl restart httpd
```
 To check the status of httpd.
```
• sudo systemctl status httpd
```
 To start the service at the time of reboot automatically then
```
 sudo systemctl enable httpd
 sudo systemctl disable httpd 
```
  
### Linux Administration – Commands Reboot
We can use following commands to reboot a server.
```
• reboot
• init 6
• shutdown -r
```
We can use following commands to shutdown a server.
```
• init 0
• shutdown -s
• halt
```
We can validate system restarted by referring the startup time.
```
• uptime
```
  
### Linux Administration – Network Commands
To check the ports which are listening in a server
```
• netstat -lntp
```
  
### Linux Administration – File Ownerships
To change the owner / group of a file
```
• chown <owner-name> file/directory
• chgrp <group-name> file/directory
• chown <owner-name>:<group-name> file/directory
```  
Note: -R option need to be used for a directory
  
### Linux Administration – File Permissions
To change the permission of a file
```
• chmod <notation> file/directory
```
Note: -R option need to be used for a directory
  
rwx    rwx   rwx
  
Owner Group Others
  
(u)    (g)   (o)
  
u+x
  
ug-o                                              +/-
  
o-rwx                                            r - > Read  
  
ugo+rwx                                          w -> write    
  
ugo+x = +x                                       x -> execute
