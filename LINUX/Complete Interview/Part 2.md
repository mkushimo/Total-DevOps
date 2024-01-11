
These Linux interview questions and answers are based on mega trending topics. If you master most of
these topics, there will be no Linux interview question that you cannot answer and secure your dream job.

## 1.What is two types of Linux User Mode ?
Command Line

GUI

## 2.What is command for created multiple files at a time?
touch

## 3.What is INODE and How to Identify?
Its unique identification code for files and directories, its was generate automatically while create new file and directories

ls -i filename

ls -ldi directoryname

## 4.List of Permissions and Users
Read, Write and Execute

Owner, Group Owners and Others

## 5.List of Special Permissions and numerical value.
Set User ID = 4

Set Group ID = 2

Stickybit = 1

## 6. What command to use see Process list in Hierarchical Structure along with PID?
Pstree -P

## 7. What is use of “top” command and how to sort Memory and User wise?
Its used to real time monitor hardware utilization of linux machine.

Press M to sort Memory wise result

Press U to sort User wise result

## 8. What is command for to force close one particular process
kill -9 Processid

## 9.What is command to refresh NIC ?
Service network restart

## 10.Tell me two types of IP Address configuration
Static IP Address

Dynamic IP Address

## 11.How do Enable / Disable Ethernet Device
Open and Edit this file #vi /etc/sysconfig/network-scripts/devicename

For enable ONBOOT = yes

For disable ONBOOT =no

## 12.What is command to change Hostname without System Restart
hostname newhostname

## 13.What is File Path of Network Configuration ?
/etc/sysconfig/network-scripts

## 14.What is File Path of DNS Configuration ?
/etc/resolv.conf

## 15.How to Update locate DB ?
cd/var/lib/mlocate

updatedb

## 16. How to edit and save file using editors?
The following commands are used to exit from vi editors.
- :wq saves the current work and exits the VI.
- :q! exits the VI without saving current work.

## 17.What is command for Zip and Unzip files
- gzip = Compress File
- gunzip = Uncompress File

## 18.What is file path of Alias name set by Permanent?
/etc/bashrc

## 19.What is MBR in linux?
Its Master Boot Recorder to help booting operating system.

## 20.What is Two Types of Mount in linux?
Temporary Mount

Permanent Mount

## 21.What is command for delete Partition?
#umount

#palimpsest &

## 22.What is command for Refresh Partition?
mount -a

## 23.What is SWAP?
Linux uses swap space to increase the amount of virtual memory available to a host. It can use one or
more dedicated swap partitions or a swap file on a regular filesystem or logical volume.

## 24.What are types can set SWAP?
Temporary set

Permanent set

## 25.What command use for Error checking and Error Fixing
fsck and e2fsck

## 26.What is PV, VG, and LVM
PV = Physical Volume

VG = Volume Group

LVM = Logical Volume

## 27.What is LVM
LVM is used to create logical partitions and during run time we can resize particular partition without data loss.

Empty partitions only can do LVM creation.

## 28.What are common commands used for Physical Volume
pvcreate

pvs

pvdisplay

## 29.What command is used for create Volume Group
vgcreate

vgs

## 30.What is Syntax for LVM Create?
#lvcreate -L partitionsize -n userdefinename volumegroupname

## 31. What types of Installation Tools in REDHAT?
RPM = Redhat Package Manager

YUM = Yellow Dog Updated Modifier
 
## 32. Tell me Linux Boot Sequence Floow?
BIOS → MBR → Boot Loader → Kernal → Runlevel

## 33. Types of Zone in DNS?
Forward lookup zone

Reverse lookup zone

## 34.What are inbuilt firwall in Linux ?
IP Tables

Selinux

TCPwrappers

## 35.What command to Execute disable IPTables permanently?
#iptables -F

Service iptables save

## 36.What is SELinux?
Its one type of firewall in linux

To block particular service in a Protocol

## 37.Location of to disable SELinux
/etc/selinux/config

## 38.What is command to check selinux status ?
getenforce

## 39.What is LDAP
The Lightweight Directory Access Protocol (LDAP) is a set of open protocols used to access centrally
stored information over a network.

## 40.Which Configuration File Is Required For Ldap Clients?
Ldap.conf
 
## 41.What Is The Name Of Main Configuration File Name For Ldap Server?
Slapd.conf

## 42.How Will You Verify Ldap Configuration File?
slaptest -u

## 43.What is command package install using YUM without ask Prompt?
yum install packagename -y

## 44. What is command Uninstall package?
yum remove packagename

## 45.What is command package re-install using YUM without ask Prompt?
yum reinstall packagename -y

## 46. Location of Cron file in linux?
/var/spool/cron

## 47.What is command for to see Particular user Job Schedule ?
crontab -lu username

## 48.What is command for restart cron service?
service crond restart

## 49.What is command for restart postfix service?
service postfix restart 50.What is command for FTP service on and restart?

chkconfig vsftpd on

service vsftpd restart

## 50. What is Kernel un Unix Operating system?
Kernel is the heart of operating system. It interacts with shell and executes the machine level language.

## 51. How can I save my input and output commands and see them when required?
At the beginning of the session if I will use SCRIPT command then the details of the input and output
commands will be saved in a file called typescript and we can view it any time using “cat typescript”
command.

This is very useful to track what user is doing what. HISTORY command will not work because it shows
data only for the current session.

## 52. How to create a file in Unix?
There are multiple way to create files in unix, but the simple way to create a file is using “cat” and “Touch”
command

Syntax:

cat > File name

touch file name

## 53. How can I check which processes are running in my machine?
To check process which are running in my machine I can use two commands. (a) TOP and (b) PS

## 54. What is the difference between TOP and PS command?
Top command gives the dynamic view of the processes are running in the server and generally the
dynamic change happens in every 3 second. Whereas PS commands gives the static view of the
processes.

## 55. You used TOP command and without aborting the TOP process I need to kill one process. Is it possible to kill ?
Yes TOP command it self has a command prompt. Type K then it will ask you for the PID of the process to
kill. Hit the PID and enter, it will kill the process.

## 56. What is the difference between creating a file in cat and in touch command?
cat command creates a file and we can save some data inside the file but touch command by default will
create a blank file.

## 57. How can I create multiple directories at a time? Say I want to create a directory D1 and inside that D2 and inside that D3. 
## Is it possible? If yes how ?
Yes creating multiple directories is possible. In this scenario the below command works.

Mkdir –p D1/D2/D3

## 58. I want to create D1, under that D2 and D3. Inside D2 I want D4 and inside D3 I want D5 to be created. How is it possible?
The below command will work for it.

mkdir –p D1/D2/D4 D1/D3/D5

## 59. How can I check in which directory I am in ?
Use PWD command to check which directory you are in.

## 60. We are using so many commands and getting output. Have you ever wondered how the commands are executing and getting you the output?
Yes every command in Unix is a C program in the backend. When we type a command and hit enter the
program runs in the backend and gives you the output.

We can view the C program as well as below.
type <Command Name> ->hit enter, it will give you a path where the program the command is located.

You can view the program by doing cat and the path name. it will open a C program file in decrypted mode.

## 61. How can I list the directories and the files ?
Using ls command. I can view the directories and files of the system.
  
## 62. How can I view hidden files in a system ?
Using ls –a command I can view the hidden files of the sytem
  
## 63. In real time environment many people use “ll” command instead of ls. So is there any command called “ll” exits?
No there is no such command called “ll”. It’s just the alias of ls command. We can check it by typing alias
command.
  
## 64. What is a shell ?
Description of shell is huge, but yes commonly we explain it as the interpreter between the user and the
machine.
  
## 65. Describe the usage of rm –r* command in unix and shall we use it in real time environment?
rm –r* will remove all the file entries in the current directory. It is not advisable to use this command in
real time environment. Specifically in production. Because we have huge files which are necessary to be
accessed by other users.
  
## 66. What is symbolic link ?
The second name of a file is called a link, it’s assigned to create another link to the current file.

## 67. What is absolute path and relative path in unix ?
Absolute path refers to the path starting from the root directory and the path continues with a sequence
starting from Root. Whereas relative path is the current path.
  
## 68. How can I check the system IP ?
type hostname command or else you can use ifconfig as well.
  
## 69. How can I check if a server is up and running or not ?
you can use ping –t command for this.
  
Ping –t <hostname> or <IP address>
  
## 70. How can I append some lines in an existing file ?
cat >> file name and hit enter. You can append lines below the existing lines of the file. And do a ctrl D to save and exit.
  
## 71. What is FIFO and LIFO in unix ?
FIFO is first in first out and LIFO is last in last out.
  
## 72. What is PATH variable ?
PATH is an environmental variable which contains the path of the command files and we can change the
paths inside the PATH variable.
  
## 73. How can I kill a process in unix?
first use PS –ef command and get the PID of the process you want to kill.
Then use kill -9 <PID_Number> command to kill the process.
  
## 74. How can I check the memory size of a linux/unix machine ?
Use Free –m or free –G command to check the memory size of a linux machine.
  
## 75. How to check disk utilization of a linux server?
Use du command to check the disk utilization.
  
## 76. How to check the disk free of all the mount points in unix ?
use df –h command, it will show the disk free of linux machine.
  
## 77. How can I check who are the users logged in my system?
use users command. It will how the details of the users logged in to the system.
  
## 78. I have a file Mantu.txt which contains multiple lines and few of the lines has a particular
## pattern as “India”. I want to print only those lines. How can I ?
I will ue grep command here. And the syntax will be as below.
Grep -i “India” Mantu.txt
  
Grep command is used for pattern earching.
  
## 79. What do you mean by a super user ?
A admin while giving permission to the users usually give normal access permission but few of the user
having special permission then normal user, they are called super user.
  
## 80. What is the syntax to move to a super user?
sudo su – <user name>
  
## 81. How can I change the permission of a file?
Using chmod command I can change the permissions of a file.
  
## 82. How can I give all permission to a user?
Use the below command to give all read, write and execute permission.
  
chmod 777 <file name>
  
## 83. What is a process group in unix ?
collection of more than one process is called as a process group in unix.the function getpgrp returns the
process group id.
  
## 84. How many numbers are used with kill while killing a process ?
there are 64 numbers which can be used with kill command but generaly we use kill -9
  
## 85. What are different types of files available in unix?
There are multiple type of files available in unix, few of among them are :
  
• Regular file
  
• Image file
  
• Binary file
  
• Linked file
  
## 86. What are cmp and different command in unix?
cmp command compares the two files byte by byte and gives the output what is not common in between
them. Diff command through the output which is not matching between the two file immediately rather
comparing bit by bit.
  
## 87. What is pipe command ? why it is used for ?
Pipe symbol interlinks two commands. It stores the output of the first command and give it to the second
command as input.
  
Cat emp.lst | mantu.txt
  
## 88. How can I number the lines of a file in VI editor?
Open the file using vi <filename>
  
Then go to command prompt and type set number. The numbers will be set before every line of the file.

## 89. What is the command to check all the options and detail information of a command in
unix ?
We can use man <command name>. it will show you all the possible way to use the command.

## 90. What is head command used for ?
head command is used to view the top portions of the file. Say if I want to view top 5 lines of a file then I
can use the below command.
  
Cat <filename> | head -5
  
## 91. What is tail command used for ?
tail command is used to view the bottom of the lines of a file. Say if I want to view bottom 5 lines of a file
then I can use the below command.
  
Cat <filename> | tail -5
  
## 92. What are the other commands used for pattern searching ?
Grep and sed are the main command used for pattern searching.
  
## 93. How can I search a pattern in vi editor ?
Open the file with vi. Use /pattern name , then hit enter, it will show you the matching patterns in VI.
  
## 94. How can I delete one line in Vi editor ?
Use dd in command mode to delete one line of a file in vi.
  
## 95. What is the command used for copying a file?
Use cp command while copying a file in unix.
  
cp <sourcepath of the file> <destination path of the file>
  
## 96. What is SCP in unix ?
Scp stands for secure copy in unix. The files which get copied by using scp command are decrypted so we
need not be worry of hacking of the file system.
  
## 97. What is mv command in unix?
We can move a file or rename a file using this command. General purpose of using mv command is to use
it for reaming purpose.
  
## 98. What does a touch command do apart from creating a blank file?
Touch command is used to change the access and modification time of the file.
  
## 99. Explain the advantages of executing a process in background
We use “&” symbol to execute a job in back ground. When we execute a job or process in unix it starts
executing in the prompt itself and we can’t do other stuffs in the command prompt at that time. So until
unless the process gets executed we have to seat idle. So for continuous interaction with the command
prompt we prefer executing the jobs or processes in back ground.
  
## 100. How do you protect file deletion in ext4?
you change any attributes of the file to read only.
  
The command is:
  
chattr +i filename
  
And to disable it:
  
chattr -i filename
  
## 101. How do you list the kerenel modules which is already loaded ?
List Currently Loaded Modules – lsmod
  
List Available Kernel Modules – modprobe -l
  
Install New modules into Linux Kernel – modprobe vmhghs
  
Remove the Currently Loaded Modul – modprobe -r vmhghs
  
## 102. What will happen in chkconfig?
issuing the command “chkconfig sendmail on” will create symlinks(softlinks)
  
/etc/rd1.d/K30sendmail
  
/etc/rd2.d/S80sendmail
  
/etc/rd3.d/S80sendmail
  
/etc/rd4.d/S80sendmail
  
/etc/rd5.d/S80sendmail
  
/etc/rd6.d/K30sendmail
  
## 103. How To rebuild Corrupted RPM Database ?
[root@tecmint]# cd /var/lib
  
[root@tecmint]# rm __db*
  
[root@tecmint]# rpm –rebuilddb
  
[root@tecmint]# rpmdb_verify Packages
  
## 104. what resize2fs do at back end?
Mounted, Extending
  
The kernel then begins writing additional filesystem metadata on the newly available storage.
  
Unmounted,Shrinking
  
resize2fs makes the filesystem use only the first size bytes of the storage. It does this by moving both
filesystem metadata and your data around.
  
After the completes, there will be unused storage at the end of the block device, unused by the
filesystem.
  
## 105. Special Permissions in linux
```
Sticky bit – Only created user and root can able to delete the file
$ chmod o+t tecadmin.txt$ chmod +t tecadmin.txt# chmod 1777 tecadmin.txt# ls -ld
tecadmin.txtdrwxrwxrwt 2 himanshu himanshu 4096 Oct 24 16:19 tecadmin.txt
SUID – Ging permission for all users like root
chmod u+s /bin/ls – ls can be used for all users as like root
# chmod 4555 [path_to_file] #ls -l /bin/ls
-rwsr-xr-x-x 1 root user 16384 Jan 12 2014 /bin/ls
SGID – SGUID :- chmod g+s /dir –> all subdirectories and files created inside will get same group
ownership as the main directory, it doesn’t matter who is creating.
chmod 2555 [dir] # ls -l /usr/bin/write
-r-xr-sr-x 1 root tty 11484 Jan 15 17:55 /usr/bin/write
```  
## 106. Password never expire linux?
```  
# chage -M -1 krishna –> set the max passwd age to -1
# passwd -x -1 krishna
chage -m 0 -M 99999 -I -1 -E -1 omadmin
```  

## 107. What files are created/modified when adding a user (useradd) in linux?
/etc/passwd and /etc/shadow
  
files from /etc/skel are typically copied into the new user’s home directory
  
## 108. How to see and get info about RAM in your system
free
  
cat /proc/meminfo
  
## 109. How will you suspend a running process and put it in the background?
Ctrl+z
  
## 110. Name the Daemon responsible for tracking System Event on your Linux box?
Syslogd
  
## 111. To see tar file without extracting?
tar -tvf
  
## 112. How to check dependencies of RPM Package on before Installing ?
```  
# rpm -qpR BitTorrent-5.2.2-1-Python2.4.noarch.rpm
/usr/bin/python2.4
python >= 2.3
python(abi) = 2.4
python-crypto >= 2.0
python-psyco
python-twisted >= 2.0
python-zopeinterface
rpmlib(CompressedFileNames) = 2.6
q : Query a package
p : List capabilities this package provides.
R: List capabilities on which this package depends.
```
  
## 113. How can we increase disk read performance in single commands?
```
To see the current read performance,
blockdev –getra /dev/sdb
256
$ time dd if=/tmp/disk.iso of=/dev/null bs=256k
2549+1 records in
2549+1 records out
copied, 6,84256 seconds, 97,7 MB/s
real 0m6.845s
user 0m0.004s
sys 0m0.865s
# After test
$ blockdev –setra 1024 /dev/sdb
$ time dd if=/tmp/disk.iso of=/dev/null bs=256k
2435+1 records in
2435+1 records out
copied, 0,364251 seconds, 1,8 GB/s
real 0m0.370s
user 0m0.001s
sys 0m0.370s
```
  
## 114. How Many Run Levels present in Linux?
There are seven run levels, with each having its own properties.
 
• Halt the system
 
• Single-user mode
 
• Multiuser mode without networking(NFS)
 
• Multi-user mode with text login
 
• Not used
 
• Multi-user mode with graphical login
 
• Reboot
  
## 115. How do i check which NFS version ?
rpcinfo -p localhost | grep -i nfs
  
rpm -qa | grep nfs
  
rpm -qi nfs nfs-utils
  
## 116. Use find command to delete file by inode?
Find and remove file using find command follows:
  
$ find . -inum 782263 -exec rm -i {} \;
  
## 117. Check if any user is using the file system?
Check to the what users are currently using the file system:
```  
# fuser -cu /dev/hdc1
/opt/backup: 2337c(root)
```
  
## 118. Explain ntsysv or chkconfig command
  
Both are similar
  
  
wat all services to start in different runlevel
  
ntsysv –level <level>
  
chkconfig –list <service name>
  
chkconfig <service name> on
  
chkconfig <service name> –level 3
  
## 119. Explained BOOT LOADER?
The boot loader is then responsible for loading the kernel
A boot loader finds the kernel image on the disk, loads it into memory, starts it.
  
Stage 1 boot loader
  
First stage the primary boot loader is to find and load the secondary boot loader
It will find by looking through the partition table for an active partition
This is verified methos to the active partition’s boot record is read from the device into RAM and
executed.
  
Stage 2 boot loader
  
The second-stage, boot loader called the kernel loader.
The first- and second-stage boot loaders combined are calledGRand Unified Bootloader.
With stage 2 loaded, GRUB can display a list of available kernels You can select a kernel parameters.
  
## 120. Explained about File System Labels?
```  
File system labels are useful where you need to address the file system that is on the device.
The file system label is set, you can use it when mounting the device.
The name replace to device by LABEL=labelname to do this
To add a lable on ext3 filesystems
# mkfs.ext3 -L mylabel /dev/sda2
To add a lable on exitsting filesystems
# tune2fs -L mylabel /dev/sda2
```
  
## 121. To convert ext2 to ext3 filesystem?
```  
# tune2fs -j /dev/hda4
```  

## 122. To convert ext3 to ext2 filesystem?
```  
# tune2fs -O^has-journal /dev/hda1
```  

## 123. To convert ext2 to ext4 filesystem?
```  
# tune2fs -O dir_index,has_journal,uninit_bg /dev/hdXX
# e2fsck -pf /dev/hdXX
```
  
## 124. To convert ext3 to ext4 filesystem?
umount /dev/sda2
  
tune2fs -O extents,uninit_bg,dir_index /dev/sda2
  
e2fsck -pf /dev/sda2
  
mount /dev/sda2 /home
  
## 125. Explained Hash Tables?
The bash shell maintains a hash table for each command which has been run. The reason, why it does so
is, making the commands run faster.
  
Whenever, a user runs a command on the shell, it first has to search the command executable as to where
is it located.
  
whenever the first time bash shell, finds the location of a command executable, it adds it to a hash table.
The next time, same command is run, the path is taken from the hash table rather than searched again making the commands run faster.
```
$ hash
hitscommand
7 /bin/grep
1 /usr/bin/which
1 /usr/bin/touch
Reset the hash table
$ hash -r
Delete the corresponding entry
$ hash -d myprint
```
  
## 126. Following the program will not affected by this shell /sbin/nologin?
FTP clients
  
mail clients
  
sudo
  
many setuid programs
  
telnet/login
  
gdm/kdm/xdm (graphical login)
  
su
  
ssh/scp/sftp etc
  
## 127. So how do I find out zombie process?
```  
# ps aux | awk ‘{ print $8 ” ” $2 }’ | grep -w Z
Output:
Z 4104
Z 5320
Z 2945
```
  
## 128. How do I kill zombie process?
```
ps axo ppid,stat | grep Z | awk ‘{print $1}’ | xargs kill -HUP
kill -HUP $(ps -A -ostat,ppid | grep -e ‘[zZ]’| awk ‘{ print $2 }’)
kill -9 $(ps -A -ostat,ppid | grep -e ‘[zZ]’| awk ‘{ print $2 }’)
To set a password to the boot loader
# grub
grub> md5crypt
Password: ************
Encrypted: $1$3yQFp$MEDEglsxOvuTWzWaztRly.
grub> quit
Next, add this to your grub.conf file like so:
default=1
timeout=10
splashimage=(hd0,0)/grub/splash.xpm.gz
password –md5 $1$3yQFp$MEDEglsxOvuTWzWaztRly.
``` 

## 129. Details about Backup?
```  
• full – as the name implies, this is a backup of everything
• differential – this is a backup of everything since the last full backup
• incremental – this is a backup of everything since the last _incremental_ backup
  
# tar -cvf /tmp/home.tar /home
This command will create a backup of /home and put that in the file /tmp/home.tar
# tar -cvf /tmp/system-backup.tar /home /var /root
create a backup of the directories /home /var /root and write that to the file /tmp/system-backup.tar
The following command makes a backup of /home and writes that to the /dev/mt0 device
# tar -cvf /dev/mt0 /home
```
  
## 130. To create a compressed archive of the directory /home
```  
# tar -zcvf /tmp/home.tar.gz /home
# tar -jcvf /tmp/home.tar.bz2 /home
```  

## 131. Extracts the contents of the compressed file
```
  # tar -zxvf /file.tar.gz
# tar -jxvf /file.tar.bz2
132. To check the contents of a tar file
# tar -tvf file.tgz
```
  
## 133. Making Device Backups Using dd
```  
# dd if=/etc/hosts of=/home/somefile
# dd if=/etc/passwd of=/home/file1
# dd if=/dev/sda of=/dev/sdb bs=4096
# dd if=backup.tar.gz of=/dev/mt0
```
  
## 134. To save MBR file backup as boot files in tmp directory
```  
# dd if=/dev/sda of=/tmp/bootfiles bs=512 count=1
```
  
## 135. Determining Filesystem Usage
To determine how much disk space is being used for a given partition, logical volume, or
NFS mount, use the df command.To display the output in “human readable” format, use the -h argument
to df.
  
The du command displays the disk usage totals for each subdirectory and finally the total usage for the
current directory.Values are in kilobytes.
  
du -hs /etc
  
du -h /vol1/group1/examplefile
  
## 136. Reporting Disk Performance
For example, if the access time for a drive suddenly drops, an administrator
must quickly start troubleshooting the problem to determine if it is a software or hardware issue or simply
due to lack of free space on the disk.
  
## 137. Displaying Memory Usage with free
```
# free -m
The free command tells you about current memory usage.
Two types of system memory exist: physical and virtual. To display the amount of free and used memory,
both physical and virtual (swap), use the free command
```  
 
## 138. Monitoring and Tuning the Kernel
Using the /proc Directory
  
Instead of executing utilities such as free and top to determine the status of system resources or fdisk to
view disk partitions, an administrator can gather system information directly from the kernel through the
/proc filesystem.
  
When you view the contents of files in /proc, you are really asking the kernel what the current state is for
that particular device or subsystem. To view the contents of a special file in /proc, use the cat, less,or more
file viewing utilities.

## 139. Network Information Service (NIS)
NIS can have only one authoritative server where the original data files are kept
This authoritative server is called the master NIS server. If your organization is large enough, you may
need to distribute the load across more than one machine. This can be done by setting up one or more
secondary (slave) NIS servers.

echo “NISDOMAIN=nis.example.org” >> /etc/sysconfig/network
  
ypserv
  
This daemon runs on the NIS server. It listens for queries from clients and responds with answers to those
queries.
  
ypxfrd
  
This daemon is used for propagating and transferring the NIS databases to slave servers.
ypbind
  
This is the client-side component of NIS. It is responsible for finding an NIS server to be queried for
information. The ypbind daemon binds NIS clients to an NIS domain. It must be running on any machines running NIS client programs.

## 140. Yum Server in linux
``` 
$ cat /etc/yum.conf
[main] cachedir=/var/cache/yum
keepcache=0
debuglevel=2
logfile=/var/log/yum.log
pkgpolicy=newest
distroverpkg=redhat-release
tolerant=1
exactarch=1
obsoletes=1
gpgcheck=1
plugins=1
metadata_expire=1800
```
 
## 141. Change User with noLogin Shell:
``` 
# useradd -s /sbin/nologin tecmint
```
 
## 142. Add a User with Home Directory, Custom Shell, Custom Comment and UID/GID
``` 
# useradd -m -d /var/www/tarunika -s /bin/zsh -c “TecMint Technical Writer” -u 1000 -g 1000 tarunika
```
 
## 143. Creating a user along with encrypted password in linux
``` 
Encrypt your password using below command
# openssl passwd -crypt mypassw0rd
Warning: truncating password to 8 characters
TuUFdiN1KaCHQ
Now you can use the encrypted the password for your new user
# useradd -p TuUFdiN1KaCHQ Deepak
``` 

## 144. Adding Information to User Account
``` 
# usermod -c “This is Tecmint” tecmint
``` 
 
## 145. Change User Home Directory
``` 
# usermod -d /var/www/ tecmint
```
 
## 146. Set User Account Expiry Date
``` 
# usermod -e 2015-03-15 tecmint
```
 
## 147. Change User Primary Group
usermod -g babin tecmint_test
 
set the babin group as a primary group to the user tecmint_test
 
## 148. Adding Group to an Existing User
usermod -G tecmint_test0 tecmint
 
new group called ‘tecmint_test0‘ to ‘tecmint‘ user
 
## 149. Change User Login Name
``` 
# usermod -l tecmint_admin tecmint
```
 
## 150. Lock User Account
```
# usermod -L babin
babin:!$1$HEWdPIJ.$qX/RbB.TPGcyerAVDlF4g.:12830:0:99999:7:::
you will see a ! added before the encrypted password in /etc/shadow file, means password disabled.
``` 
 
## 151. Unlock User Account
``` 
# usermod -U babin
babin:$1$HEWdPIJ.$qX/RbB.TPGcyerAVDlF4g.:12830:0:99999:7:::
```
 
## 152. Change User Shell
``` 
# usermod -s /bin/sh babin
```
 
## 153. Change UID and GID of a User
``` 
# usermod -u 666 -g 777 jack
```
 
## 154. To check on the status of our RAID device
``` 
# mdadm –query –detail /dev/md0
# cat /proc/mdstat
```
 
## 155. To create RAID disk
```
# mdadm –create /dev/md0 -l 1 -n 3 /dev/sda{5,6,7}
# mdadm –create /dev/md0 -l 1 -n 3 /dev/sda /dev/sdb /dev/sdc -x 2 /dev/sdd
```
 
## 156. To create RAID disk with spare disk
```
# mdadm –create /dev/md0 -l 1 -n 2 /dev/sda{5,6,} -x 1 /dev/sda7
# mdadm –manage /dev/md0 –stop
# mdadm –create /dev/md0 -l 5 -n 3 /dev/sda{5,6,7} -x 1 /dev/sda8
x———> spare-devices
```
 
## 157. To create LVM on RAID 1 disk
``` 
# pvcreate /dev/md0
# vgcreate datavg /dev/md0
# lvcreate -L +1G -n /dev/datavg/datalv
```
 
## 158. Disk Failure on RAID
```
To simulate a disk failure, we’ll use mdadm to tell the kernel that /dev/sdb1 has failed
# mdadm –manage /dev/md0 –fail /dev/sda7
# cat /proc/mdstat
sda7 [F]
```
 
## 159. How do remove failed disk from the RAID array
``` 
# mdadm –manage /dev/md0 –remove /dev/sda7
```
 
## 160. To add raid device
```
# mdadm –manage /dev/md0 –add /dev/sda9
```
 
## 161. To quickly check the state of all your RAID arrays
``` 
# cat /proc/mdstat
```
 
## 162. userlist_enable vsftpd
```
Will load a list of usernames from the filename specified by the userlist_file directive when this option is
enabled. And if a user tries to log in using a name in this file, that user will be denied access before even
being prompted for a password. The default value is NO.
```
 
## 163. userlist_deny
This option is examined if the userlist_enable option is active. When its value is set to NO, users will be
denied login, unless they are explicitly listed in the file specified by userlist_file. When login is denied, the
denial is issued before the user is asked for a password; this helps prevent users from sending clear text
across the network. The default value is YES.
 
## 163. userlist_file
This option specifies the name of the file to be loaded when the userlist_enable option is active. The
default value is vsftpd.user_list.
 
## 164. download_enable
If set to NO, all download requests will be denied permission. The default value is YES.
 
## 165. write_enable
This option controls whether any FTP commands that change the file system are allowed.
These commands are used STOR, DELE, RNFR, RNTO, MKD, RMD, APPE, and SITE.
The default value is NO.
 
## 166. UserDir
This directive defines the subdirectory within each user’s home directory, where users
can place personal content that they want to make accessible via the web server. This
directory is usually named public_html and is usually stored under each user’s home
directory. This option is, of course, dependent on the availability of the mod_userdir
module in the web server setup.
 
A sample usage of this option in the httpd.conf file is:
 
UserDir disable
 
UserDir public_html
 
## 167. ErrorDocument
The ErrorDocuments directive lets you specify what happens when a client asks for a
nonexistent document.
 
Specifies a file that the server sends when an error of a specific type occurs. 
You can also provide a text message for an error. Here are some examples:
``` 
ErrorDocument 403 “Sorry, you cannot access this directory”
ErrorDocument 403 /error/noindex.html
ErrorDocument 404 /cgi-bin/bad_link.pl
ErrorDocument 401 /new_subscriber.htm
• 400: Bad Request
• 401: Unauthorized
• 402: Payment Required
• 403: Forbidden
• 404: Not Found
• 405: Method Not Allowed
• 406: Not Acceptable
• 407: Proxy Authentication Required
• 408: Request Timeout
• 409: Conflict
• 410: Gone
• 411: Length Required
• 412: Precondition Failed
• 413: Request Entity Too Large
• 414: Request-URI Too Long
• 415: Unsupported Media Type
• 416: Requested Range Not Satisfiable
• 417: Expectation Failed
• 500: Internal Server Error
• 501: Not Implemented
• 502: Bad Gateway
• 503: Service Unavailable
• 504: Gateway Timeout
• 505: HTTP Version Not Supported
```
 
## 168. How to connect to a specific share using smbclient, use the following:\
``` 
# smbclient //<servername>/<sharename> -U <username>
# smbclient //192.168.10.10/data -U edward
# vim /etc/samba/smb.conf
workgroup=WORKGROUP
hosts allow = <IP addresses>
comment
Brief description of the share displayed when browsing for the share.
valid users
List of Samba users allowed access to the share.
invalid users
List of Samba users denied access the share. If a user is listed in the
valid users and the invalid users list, the user is denied access.
public
If set to yes, password authentication is not required. Access is granted
through the guest user with guest privileges. (default=no)
read only
If set to yes, client users can not create, modify, or delete files in the share. (default=yes)
printable
If set to yes, client users can open, write to, and submit spool files on the shared directory. (default=no)
hosts allow
List of clients allowed access to share. Use the command man 5 hosts_access for details on valid
IP address formats.
browseable
If set to no, the share will not be visible by a net view or a browse list.
```
 
## 169. Find Files Using Name in Current Directory?
```
# find . -name tecmint.txt
```
 
## 170. Find Files Under Home Directory?
```
# find /home -name tecmint.txt
```
 
## 171. Find all PHP Files in Directory?
``` 
# find . -type f -name “*.php”
```
 
## 172. Find Files Without 777 Permissions?
``` 
# find / -type f ! -perm 777
```
 
## 173. Find SGID Files with 644 Permissions?
``` 
# find / -perm 2644
```
 
## 174. Find Sticky Bit Files with 551 Permissions?
``` 
# find / -perm 1551
```
 
## 175. Find SUID Files?
``` 
# find / -perm /u=s
```
 
## 176. Find SGID Files?
```
# find / -perm /g=s
```
 
## 177. Find Read Only Files?
```
# find / -perm /u=r
```
 
## 178. Find Executable Files?
```
# find / -perm /a=x
```
 
## 179. Find all Empty Files?
```
# find /tmp -type f -empty
```
 
## 180. Find all Empty Directories?
```
# find /tmp -type d -empty
```
 
## 181. File all Hidden Files?
``` 
# find /tmp -type f -name “.*”
```
 
## 182. Find Single File Based on User?
``` 
# find / -user root -name tecmint.txt
```
 
## 183. Find all Files Based on User?
```
# find /home -user tecmint
```
 
## 184. Find all Files Based on Group?
```
# find /home -group developer
```
 
## 185. Find Last 50 Days Modified Files?
```
# find / -mtime -50
```
 
## 186. Find Last 50 Days Accessed Files?
```
# find / -atime -50
```
 
## 187. Find Last 50-100 Days Modified Files?
```
# find / -mtime +50 –mtime -100
```
 
## 188. Find Changed Files in Last 1 Hour?
```
# find / -cmin -60
```
 
## 189. Find Modified Files in Last 1 Hour?
```
# find / -mmin -60
```
 
## 190. Find Accessed Files in Last 1 Hour?
```
# find / -amin -60
```
 
## 191. Find 50MB Files?
```
# find / -size 50M
```
 
## 192. Find using inode number?
```
find . -inum 27492358 -exec rm -i {} \;
```
 
## 193. Main configuration file of Apache server?
/etc/httpd/conf/httpd.conf
 
## 194. Main configuration file of Apache server?
/etc/httpd/conf/httpd.conf
 
## 195. Specify number of maximum open files in a single login based on the amount of system RAM.
```
#echo “1599383” > /proc/sys/fs/file-max
This can also be done by using sysctl
sysctl command is used to change Kernel Parameters at run-time
#sysctl -w fs.file-max=1599383
Kernel Parameters can also be changed by making changes in the below file:
/etc/sysctl.conf
Append the below line in the /etc/sysctl.conf file
fs.file-max = 1599383
After making the above change run the below command for changes to reflect, loads the sysctl settings
#sysctl -p
```
 
## 196. Increase the local port range, by default the port range is small?
```
#echo “1024 65535″ > /proc/sys/net/ipv4/ip_local_port_rangeThis can also be done using sysctl command
#sysctl -w net.ipv4.ip_local_port_range=”1024 65535”
Append the below line in the /etc/sysctl.conf file
net.ipv4.ip_local_port_range = 1024 61000
After making the above change run the below command for changes to reflect, loads the sysctl settings
#sysctl –p
```
 
## 197. Disable packet_forwarding(routing)?
```
net.ipv4.ip_forward = 0
#cat /proc/sys/net/ipv4/ip_forward
```
 
## 198. Mount file systems with noatime options?
```
noatime option means it will not update the file and directory access time.
Main advantage is I/O performance will increase.
```
 
## 199. Which command is use to extend a logical volume?
```
lvextend –size +<addsize> /dev/<vgname>/<lvname>
resize2fs /dev/<vgname>/<lvname>
lvextend -L +1G /dev/VolGroup/LogVol1
This will extend the partition size by +1 GB
resize2fs /dev/VolGroup/LogVol1
```
 
## 200. ServerAdmin : Email address
This is the e-mail address that the server includes in error messages sent to the client.
 
Defines the e-mail address that is shown when the server generates an error page.
 
The e-mail address that the Web server provides to clients in case any errors occur.
 
## 201. What is the use of SCP command in Linux?
SCP command stands for secure copy. It is used to copy/download data from one machine to another
machine.
 
## 202. What is telnet and what does it do?
the telnet command is used to check the connectivity to other servers. It helps you to check whether you
are able to talk to another server or now. Ex: telnet 192.0.0.1 22 where 22 is the port number.
 
## 203. What is a bastion host?
A bastion host is also known as a jump server. It is used to connect from one machine to another machine
securely. Bastion hosts are used to connecting to private servers securely.
 
## 204. What is the command to find the IP address of the host machine in linux?
You can use ifconfig/ ipaddr show command to find the IP address of the host machine.
 
## 205. Name some of the text editors that are available in Linux?
Some of the common text editors that are available in Linux are vi/vim, nano, subl, gedit, atom, emacs. Vi
is the default editor that you have in Linux machines.
 
## 206. What are the different zip files formats that are available in linux?
The different zip formats in Linux are zip, gzip and bzip.
 
## 207. What is the difference between cp and mv command?
cp command stands for copy and is used to copy data from one location to another. mv stands for the
move and is used to move data from one location to another.
 
## 208. How can you run a process in the background in Linux?
You can run a process in the background by pressing ctrl+z command.
 
## 209. What is the use of ‘chown’ command ?
chown stands for ‘change ownership’ and is used to change the ownership of a file or directory. Eg:
chown username.username <filename>.
 
## 210. What is the use of ‘chmod’ command?
chmod stands for ‘change mode’ and is used to change the permissions on files or directories. Eg: chmod
a+w <filename>
 
## 211. What is the command to create a zip file in linux?
To create a zip file you can use tar command with -cvzf arguments. Eg: tar -cvzf test.tar.gz <file names to
be included in the zip>
 
## 212. What is the command to unzip the file in linux?
To unzip a file you can tar command with -xvzf arguments. Eg: tar -xvzf test.tar.gz
 
## 213. What is the command to show the contents of a zip file ?
To see the contents of the zip file you can use tar -tvzf arguments. Eg: tar -tvzf test.tar.gz
 
## 214. What is a soft link in Linux?
A soft link is used to create a shortcut in Linux. This is similar to creating a shortcut in windows systems.
 
## 215. What is the command used to create a soft link?
To create a soft link you can use ln command with -s arguments. Eg: ln -s /var/www/html html, where
/var/www/html is the source file and HTML is the destination of the shortcut.
 
## 216. What is the command to remove the soft link in Linux?
To remove the soft link in Linux you can use unlink command. Eg: unlink <filename>
 
## 217. What is the use of whereis command in linux?
Whereis command is used to find the binaries and libraries files of an application in linux.
 
## 218. What is the use of man pages?
Man pages stand for manual pages. It is the documentation about and helps you to understand the
commands and how to use the commands. Eg: man wget.
 
## 219. what does “2>” indicate in redirection?
This means that output will be shown on the screen and the errors will be written to a file that you specify.
Eg: ls /etc/test 2> error.txt
 
## 220. What are the different type of users that you have in Linux?
You have 2 types of users in linux. They are
• root user
 
• standard users.
 
Linux System Administration Interview Questions and Answers
 
### 221. How To check Memory stats and CPU stats ?
free & vmstat commands.
 
## 222. What is the purpose of runlevels ?
Useful for debugging purpose. Basic idea is each runlevel has some services operational and depending
on need can enable different runlevels to test which services are running
 
## 223. You are able to ping with a numeric IP address, but not by name. How will you debug ?
First check /etc/resolv.conf file for DNS Server Entry
 
## 224. Generally setting up services in Linux require ————— and ————–
Update the associated configuration file and ensure the appropriate daemon is started
 
## 225. What is the purpose of iptables command ?
Basically allows rule creation to filter packets according to established criteria. Network Address
Translation function is also done
 
## 226. You are noticing mails are not sent by sendmail. Where can you find the error log to see what happened ?
/var/spool/mail/
 
## 227. How can you findout the current runlevel the system is in ?
who -r
 
## 228. Linux system has crashed and keeps getting to the # Debug Prompt. How do you bring it to normal login prompt?
Likely due to file system inconsistency, run fsck to check and accept inode repairs.

## 229. How can you customise startup settings for your login in bash shell
Update .bashrc
 
## 230. What is the first process started by the Scheduler
init
 
## 231. How can you find the current status of Virtual memory in the Linux System ?
cat /proc/meminfo * Note the very useful /proc filesystem
 
## 232. Hardware devices are identified as special files in Linux. Name the types
Character,block and Network
 
## 233. Name 3 Environment variables
SHELL,HOME,PATH
 
## 234. Where is my vmlinuz executable loaded from ?
/boot
 
## 235. As System Administrator you have to apply a patch that is in .tar.gz format. How would you use it ?
Get the file and apply tar -zxvf <filename.tar.gz>
 
## 236. What are Kernel types and which one is Linux ?
Monolithic and Micro. Linux is a Monolithic Kernel.
 
## 237. As System Admin, log files are monitored as they grow. How is this achieved ?
tail -f
 
## 238. Automatic mounting of new file system at boot-time can be done by
Adding an entry in /etc/fstab file
 
## 239. You recently ran an install, the command for which you need to recall. How do you get this?
history command
 
## 240. In writing a Bash Shell script, special character’ meaning has to be altered. How is it done?
Escape sequence. Precede the special character with a ‘\’
 
## 241. Linux associates devices with File Descriptors. List them
0 – Standard Input. 1- Standard Output 2-Standard Error
 
## 242. How do you set a mask to stop certain permissions from being granted by default on file creation?
umask command
 
## 243. You want to try out a Distribution before installation. Which image would suit?
LiveCD
 
## 244. System Administrators monitor load averages on System for analysis. How is this done?
top command
 
## 245. What is the behaviour of the following very useful grep command ?
grep [abc] file1 : Looks for matches in file1 containing either an a or b or c character.
 
## 246. You need to make a file with only read permissions for yourself, group and all. How can you ?
chmod 444 file1
 
## 247. What does su – do ? Give an example of when you would use this.
Gets the switch to root account. Need to be done before Software installation.
 
## 248. Pipe is a very important concept in process communication. Give an example?
cat file1 |grep xyz : Pattern matching by grep happens on the displayed file1
 
## 249. In Shell scripting command return codes are checked prior to proceeding. Explain?
These are Exit status codes. Linux follows 0 for success and nonzero codes for failures
 
## 250. Signals is one way that process communication happens in Linux. What does ctrl C do ?
Generates a SIGINT signal that stops the current process running in the shell.
(* RedHat Based Systems. )
