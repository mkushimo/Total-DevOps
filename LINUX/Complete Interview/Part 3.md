# Linux 200+ Technical Interview Questions:
In some questions I am encouraging to search online because it will help you practice for
searching more complicated questions in the future

(Good Luck)

## 1. When you login you get “$” prompt, what is the prompt for root?
```
#
```

## 2. Explain the difference between grep and egrep?
Search online

## 3. What is the port # for DNS, NTP and NFS?
53,123 and 111/2049

## 4. What is the configuration file name of DNS and where is it located?
/etc/named.conf

## 5. How many new directories will be created after running the following command?
mkdir {a..c}{1..3}

9

## 6. Your PC is configured with a DNS server address but not the default gateway. Can the PC access internet?
No

## 7. What is the difference between IP and Gateway?
Search online

## 8. Can you assign one static IP to 2 computers, if not then why?
No because it will create IP conflict

## 9. How to change IPs address to static?
ifconfig x.x.x.x

## 10. You are trying to ping a server by hostname and you get an error message, “ping: unknown host …”. What could be the reason and
## how to solve the problem so you can ping it by hostname?
Check for /etc/hosts or DNS to see if it has hostname to IP entry

## 11. Explain the difference between relative and absolute path?
Absolute path starts from / where relative path is your current directory

## 12. List 3 different methods of adding user?
Search online

## 13. What is the command to change file/directory ownership and group?
chown and chgrp

## 14. List any 3 type of filesystem?
ext4,NTFS and FAT

## 15. When you login you get a message on the screen. What is the name of that file and where is it located?
/etc/motd

## 16. What is /bin directory used for?
Search online

## 17. What are the different types of DNS Server
Master and secondary

## 18. How to change a user password?
passwd username

## 19. What is the version of Redhat Linux you have experience with?
7.4

## 20. List any 4 linux distributions?
Redhat, CentOS, Ubuntu and SUSE

## 21. How to logoff from the system?
exit

## 22. Give any 3 examples of operating systems?
Windows, Linux and MAC

## 23. How to create a directory?
mkdir

## 24. Where are the zone files located for DNS service?
/var/named/zonefiles

## 25. How to check kernel version?
uname –a

## 26. Which directory has all the configuration files?
/etc

## 27. How to become root user from a regular user?
su –

## 28. How many mega bytes in 1 giga bytes?
Search online

## 29. What is the purpose of having different network ports?
So the communication of each application goes through a dedicated port

## 30. How to display first column of a file?
cat filename | awk ‘{print $1}’

## 31. What is the name of DNS rpm package?
bind

## 32. What is the difference between nslookup and dig commands?
Search online

## 33. How to check your user id and group id?
id

## 34. How to check a file’s permission?
ls –l

## 35. What is the difference between “kill” and “kill -9” command?
Search online

## 36. What is subnet?
Search online

## 37. You are troubleshooting an issue with Redhat support and they have asked you to send the contents of /etc directory. How and
## which method you will use to transfer the contents?
tar (compress) the entire /etc directory and ftp

## 38. What is root home directory?
/root

## 39. What is rsyslogd deamon and its purpose?
Search online

## 40. Your company has terminated a server administrator. What is first thing as an administrator you should do to enhance the security?
Change root password

## 41. How to check the computer name or host name in Linux?
hostname

## 42. Which permission allows a user to run an executable with the permissions of the owner of that file?
First 3 bits should have x

## 43. What is the command to untar a tarred file?
untar

## 44. What is /proc directory used for?
Search online

## 45. What is the purpose of nsswitch.conf file
It tells the system where to go to resolve hostnames

## 46. List 3 basic commands to navigate the filesystem?
cd, pwd and ls

## 47. Which service/daemon should be running on the server that allows you to connect remotely?
sshd

## 48. What is the purpose of firewall?
Search online

## 49. List any 3 IT components?
Hardware, OS and Applications

## 50. Which directory has all the commands we use, e.g. ls, cd etc.?
/usr/bin or /bin

## 51. What is the difference between memory, virtual memory and cache?
Search online

## 52. Which of the following is correct?
a. Hardware => Operating System => Users

b. Operating System => Users => Hardware

c. Database => Hardware => Users

## 53. Which of the following is a communication command?
- grep

- mail

- touch

- cd

## 54. How to rename a file or directory?
mv

## 55. How to change a hostname in Linux?
Search online

## 56. How to check network interfaces in Linux?
ifconfig

## 57. Why is “tail –f logfilename” command used most often and what does it do?
It will output all incoming logs in real time

## 58. What type of hardware have you worked on?
You should get yourself familiar with Dell, HP and UCS hardware by going online and check the vendor websites

## 59. How to sort a file in reverse order?
cat filename | sort –r

## 60. What is the name of operating system that runs Unix?
Solaris, HP-UX etc.

## 61. List all byte sizes from smallest to largest?
Search online

## 62. How to check the total number of partition in Linux?
fdisk -l

## 63. How to access a linux system from a linux system?
ssh

## 64. Explain the procedure of bonding 2 NICs or interfaces together?
Search online

## 65. What is the exact command syntax to list the 5th column of a file and cut the first 3 letters?
cat filename | awk ‘{print $5}’ | cut –c1-3

## 66. What is /etc/hosts file used for?
To resolve hostnames with IP address

## 67. List any 3 options of ‘df’ command and what they are used for?
Search online

## 68. What is the command to change file/directory permissions?
chmod

## 69. What is the purpose of pipe (|)?
To combine multiple commands

## 70. What is /etc directory used for?
For configuration files

## 71. Which command is used to list files in a directory?
ls –l

## 72. There is a command which gives you information about other commands, please explain that command and what is it used for?
man

## 73. How to delete a file and a directory?
rm filename and rmdir dirname

## 74. What is the difference between “tail” and “tail -10”?
None

## 75. List 4 commands to display or read a file contents?
cat, more, less, vi

## 76. Which command is used to read the top 5 lines of a file?
head -5 filename

## 77. What are the different commands or methods to write to a file?
echo > filename and vi filename

## 78. What is swap space and how to check swap space?
Search online

## 79. What is inode and how to find an inode of a file?
Search online

## 80. Which file to edit for kernel tuning?
Search online

## 81. What is the latest version of Redhat?
Search online

## 82. Name the command to find specific word from a file?
grep word filename

## 83. You have scheduled a job using crontab but it does not run at the time you specified, what could be the reason and how would you troubleshoot?
Check your system time

Check your crontab entry

Check /var/log/messages

## 84. How to check system hardware information?
dmidecode

## 85. How to check network interface MAC address?
ifconfig

## 86. If I don’t want others to read my file1, how to do that?
Remove r from the last 3 bits of file permission

## 87. What is the purpose of “uniq” and “sed” command?
Search online

## 88. Which command is used to list the contents of a directory in the most recent time and in reverse order, meaning the most updated
## file should be listed on the bottom?
ls –ltr

## 89. What is the difference between tar, gzip and gunzip?
Search online

## 90. What are the different ways to install and OS?
DVD, DVD iso and network boot

## 91. How to view difference between two files?
diff file1 and file2

## 92. You noticed that one of the Linux servers has no disk space left, how would you troubleshoot that issue?
If running LVM then add more disk and extend LVM

If not running LVM then add more disk, create a new partition and link the new partition to an existing filesystem

## 93. How to check Redhat version release?
uname –a or /etc/redhat-release

## 94. What is the difference between TCP and UDP?
Search online

## 95. What is a zombie process?
Search online

## 96. How do you search for a pattern/word in a file and then replace it in an entire file?
sed command

## 97. Explain the purpose of “touch” command?
To create an empty file

## 98. If a command hangs, how to stop it and get the prompt back?
Ctrl C

## 99. Which command is used to count words or lines?
wc

## 100. How to check the number of users logged in?
who

## 101. What is the command to view the calendar of 2011?
cal 2011

## 102. Which command is used to view disk space?
df –h

## 103. How to create a new group in Linux?
groupadd

## 104. What is the command to send a message to everyone who is logged into the system?
wall

## 105. Which command is used to check total number of disks?
fdisk –l

## 106. What is an mail server record in DNS?
MX

## 107. What does the following command line do?
ps -ef | awk '{print $1}' | sort | uniq

List the first column of all running processes, sort them and remove duplicates

## 108. You get a call that when a user goes to www.yourwebsite.com it fails and gets an error, how do you troubleshoot?
Check for user internet

Check to see if user computer has DNS for hostname lookup

Check to see if the server is up that is running that website

Check to see if the server’s web service is running

Check for DNS availability which is resolving that website

## 109. List 4 different directories in /?
/etc, /bin, /tmp, /home

## 110. What is the output of the following command:
$tail -10 filename | head -1

It will show the first line from the last 10 lines of a file

## 111. What are the different fields in /etc/passwd file?
Search online

## 112. Which command is used to list the processes?
ps –ef

## 113. What is the difference between “hostname” and “uname” commands?
Hostname will give you system name and uname will give you OS information

## 114. How to check system load?
top and uptime command

## 115. How to schedule jobs?
crontab and at

## 116. What is the 3rd field when setting up crontab?
Day of the month

## 117. What is the command to create a new user?
useradd

## 118. What is the “init #” for system reboot?
6

## 119. How to restart a service?
systemctl restart servicename

## 120. How to shutdown a system?
shutdown or init 0

## 121. What is “ftp” command used for?
To transfer files from one computer to another

## 122. Explain cron job syntax? First is minute, second is..?
Min, house, day of the month, month, day of the week and command

## 123. How to delete a package in Linux?
rpm –e packagename

## 124. What is the file name where user password information is saved?
/etc/shadow

## 125. Which command you would use to find the location of chmod command?
which chmod

## 126. Which command is used to check if the other computer is online?
ping othercomputer

## 127. Please explain about LAN, MAN and WAN?
Search online

## 128. How to list hidden files in a directory?
ls –la

## 129. What is the difference between telnet and ssh?
ssh is secure where telnet is not

## 130. How to run a calculator on Linux and exit out of it?
bc and quit

## 131. List any 4 commands to monitor system?
top, df –h, iostat, dmesg

## 132. You are notified that your server is down, list the steps you will take to troubleshoot?
Check the system physically

Login through system console

Ping the system

Reboot or boot if possible

## 133. What is difference between static and DHCP IP?
Search online

## 134. How to write in vi editor mode?
i => insert,   a => insert in next space,   o => insert in new line

## 135. What is the difference between “crontab” and “at” jobs?
crontab is for repetitive jobs where at is for one time job

## 136. What is vCenter server in VMWare?
Search online

## 137. What is “dmidecode” command used for?
To get system information

## 138. What is the difference between SAN and NAS?
Search online

## 139. What is the location of system logs? E.g. messages
/var/log directory

## 140. How to setup an alias and what is it used for?
alias aliasname=”command”

It is used to created short-cuts for long commands

## 141. What is the purpose of “netstat” command?
Search online

## 142. What are terminal control keys, list any 3?
Crtl C, D and Z

## 143. Which command(s) you would run if you need to find out how many processes are running on your system?
ps –ef | wc –l

## 144. What are the different types of shells?
sh, bash, ksh, csh etc.

## 145. How to delete a line when in vi editor mode?
dd

## 146. Which is the core of the operating system?
a) Shell

b) Kernel

c) Commands

d) Script

# 147. Which among the following interacts directly with system hardware?
a) Shell

b) Commands

c) Kernel

d) Applications

## 148. How to save and quit from vi editor?
Shift ZZ or :wq!

## 149. What is the difference between a process and daemon?
Search online

## 150. What is the process or daemon name for NTP?
ntpd

## 151. What are a few commands you would run if your system is running slow?
top, iostat, df –h, netstat etc.

## 152. How to install a package in Redhat Linux?
yum install packagename

## 153. What is the difference between “ifconfig” and “ipconfig” commands?
ifconfig for Linux and ipconfig for Windows

## 154. What is the first line written in a shell script?
Define shell

e.g. #!/bin/bash

## 155. Where is the network (Ethernet) file located, please provide exact directory location and file name?
/etc/sysconfig/network-scripts/ifcfg-nic

## 156. Why do we use “last” command?
To see who has logged in the system whether active or logged off

## 157. What is RHEL Linux stands for?
Search online

##  158. To view your command history, which command is used and how to run a specific command?
history and history #

## 159. What is NTP and briefly explain how does it work and where is the config files and related commands of NTP?
Search online

## 160. How to disable firewall in Linux?
Search online

## 161. How to configure mail server relay for sendmail service?
Edit /etc/mail/sendmail.mc file and add SMART_HOST entry

## 162. Where is samba log file located?
/var/log/samba

## 163. What is mkfs command used for?
To create a new filesystem

## 164. If you create a new group, which file does it get created in?
/etc/group

## 165. Which file has DNS server information (e.g. DNS resolution)?
/etc/resolv.conf

## 166. What are the commands you would run if you need to find out the version and build date of a package (e.g. http)?
rpm –qi http

## 167. On the file permissions? What are the first 3 bits for and who is it for?
Read, write and execute. They are used for the owner of the file

## 168. How to create a soft link?
ln –s

## 169. How to write a script to delete messages in a log file older than 30 days automatically?
Search online

## 170. How to quit out of “man” command?
q

## 171. Which command is used to partition disk in Linux?
fdisk

## 172. What is the difference between “shutdown” and “halt” command?
Search online

## 173. What is the exact syntax of mounting NFS share on a client and also how to un-mount?
Search online

## 174. What experience do you have with scripting, explain?
if-the, do-while, case, for loop scripts

## 175. How to get information on all the packages installed on the system?
rpm –qa

## 176. Explain VMWare?
Search online

## 177. You are tasked to examine a log file in order to find out why a particular application keep crashing. Log file is very lengthy,
## which command can you use to simplify the log search using a search string?
grep for error, warning, failure etc. in /var/log/messages file

## 178. What is /etc/fstab file and explain each column of this file?
Search online

## 179. What the latest version of Windows server?
Search online

## 180. What is the exact command to list only the first 2 lines of history output?
history | head -2

## 181. How to upgrade Linux from 7.3 to 7.4?
yum install update

## 182. How to tell which shell you are in or running?
$0

## 183. You have tried to “cd” into a directory but you have been denied.
You are not the owner of that directory, what permissions do you need and where?
- - - - - - - r – x

## 184. What is CNAME record in DNS?
Entry for hostname to hostname

## 185. What is the name of VMWare operating system?
ESXi

## 186. What is the client name used to connect to ESXi or vCenter server?
vSphere client

## 187. You get a call from a user saying that I cannot write to a file because it says, permission denied. The file is owned by that user, how do you troubleshoot?
Give write permission on the first 3 bits

## 188. What is the latest version of VMWare?
Search online

## 189. What is the name of firewall daemon in Linux?
firewalld

## 190. Which command syntax you can use to list only the 20th line of a file?
Search online

## 191. What is the difference between run level 3 and 5?
3 = Boot system with networking, 5 = boot system with networking and GUI

## 192. List a few commands that are used in troubleshooting network related issue?
netstat, tcpdump etc.

## 193. What is the difference between domain and nameserver?
Search online

## 194. You open up a file and it has 3000 lines and it scrolled up really fast, which command you will use to view it one page at a time?
more or less

## 195. How to start a new shell. E.g. start a new ksh shell?
Simply type ksh, or bash

## 196. How to kill a process?
kill processID

## 197. How to check scheduled jobs?
crontab –l

## 198. How to check system memory and CPU usage?
free and top

## 199. Which utility could you use to repair the corrupted file system?
fsck

## 200. What is the command to make a service start at boot?
systemctl enable servicename

## 201. How to combine 2 files into 1? E.g. you 3 lines in file “A” and 5 lines in file “B”, which command syntax to use that will combine into one file of 3+5 = 8 lines
cat fileA >> fileB

## 202. What is echo command used for?
To output to a screen

## 203. What does the following command do?
echo This year the summer will be great > file1

It will create a new file “file1” with the content as “This year the summer will be great”

## 204. Which file to modify to allow users to run root commands
/etc/sudoers

## 205. You need to modify httpd.conf file but you cannot find it, Which command line tool you can use to find file?
find / -name “httpd.conf”

## 206. Your system crashed and being restarted, but a message appears, indicating that the operating system cannot be found. What is the most likely cause of the problem?
The /boot file is most likely corrupted
