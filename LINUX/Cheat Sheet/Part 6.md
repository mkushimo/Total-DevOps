# Linux Basics
# Linux

### 1. Creating File without data 
```
Single file : touch <filename>.<extension>
Multiple files : touch <file1> <file2><file3>...
```

### 2. Creating file with minimal data echo 
```
“Hii ! , This is Data” > <filename2>.<extension>
```
### 3.  Adding extra data to existing file 
```
echo “Hii ! , This is Extra Data” >>
<filename2>.<extension>
```

### 4. To Replace the existing data :
```
 echo “Hii ! , This is Replacing Data”>
<filename2>.<extension>
```

### 5. Move file 
```
 mv <filename> <folder-location/directory>
```

### 6. Copy file 
```
cp <filename> <location where you need to copy>
```

### 7. Rename file 
```
mv <filename> <newfilename>
```

### 8. Remove file 
```
rm <filename>
```

### 9. Find file 
```
find <directory> -name <name-of-file>
```

### 10. Locate file (search with keyword
without directory)
```
i) update db : sudo updatedb && locate -e
bench-repo
ii) locate <keyword/filename/foldername>
```

### 11. File edit using VI Editor (existing file) 
```
vi <filename+extension if its having>
```

### 12. Basic VI Editor Keystrokes :
```
 To Enter into Input mode / to add data/txt : type I
To Delete backward : backspace
To add next line : enter
To Save file : Click ESC , and type wq! Enter (means write quite)
```

## Linux Directories - read

### 1. To Read File 
```
cat <filename>
```

### 2. To Read Top 5 lines 
```
head -5 <filename>
```

### 3. To Read bottom 6 lines
```
tail -6 <filename>
```

### 4. To Read File with line number 
```
cat -n <filename>
```

### 5. Copy content from old file to new
```
Cat <oldfile > > <newfile>
```

### 6. Add multiple files data into one 
```
cat <file1> <file2 >... > <newfilename>
```

### 7. Reverse line reading 
```
tac <filename>
```

### 8. Read sufficient in screen size 
```
more <filename>
```

### 9. Read with search
```
less <filename> ,next /<enter text to search>
```

### 10. Word count 
```
wc <filename>
```


## Linux Directories
### 1. Creating Directory/Folder 
```
mkdir <folder-name>
```

### 2. Removing Directory 
```
rmdir <directory/folder name>
```

### 3. To know present directory 
```
pwd
```

### 4. Moving directory / Cut 
```
mv <old-dir> <new-dir>
```

### 5. Copy directory / Copy 
```
Cp -R <dir> <new-dir-location>
```

### 6. To go to home directory
```
 cd
```

### 7. To go to particular directory 
```
cd </directory/subdir-directory-location>
```

### 8. To go backward directory 
```
cd ..
```

### 9. Create directory within another 
```
dir mkdir -p <dir1/dir2/dir3> (inside dir3 dir
will be created)
```

### 10. Remove Directory inside directories 
```
Rmdir -R <directory name>
```

### 11. To see hidden directories
```
dir -a
```

### 12. To see which user created dir 
```
dir -l --author
```


## Linux Directories - Listing
|  |  |
| :--- | :--- | 
|Listing directories |  ls |
| Long listing | ll |
| Listing with hidden/all | ls -a |
| Long with hidden file | ll -a |
| Listing with human readable(memory in kb,mb,gb) | ll -lh |
| Listing with human readable(memory in MB),G for GB,T for TB | ls -l --block-size=M |
| Listing with index | ls -li |
| Listing with reverse order of name | ls -llr |
| Listing directories along with directories | ls -R |


## Linux listing directory explanation
-rw-rw-r--. 1 opc opc 0 Sep 5 02:31 file2

| Filetype + users permission | Index /links | owner | user | size | date | time | File name |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| - rw-rw-r– | 1 | opc | opc | 0 | Sep 5 | 02:31 | file2 |


|  |  |  |  |
| :--- | :--- | :--- | :--- |
| File Types ( first letter ) |  - : file | d : directory | l: link |
| File Permissions | r → read | w → write | e → execute |
| rw- rw- r– ( - means no permission) | first three for owner | next : group | last : other users |


## Linux Users

### Current logged in username 
```
whoami
```
### All users logged in to system 
```
who
```
### To find user id 
```
id
```
### To see logged in users along with from where they logged in 
```
w
```
### Switch to another user, you need to know password for user 
```
su <username>
```
### Switch to another user with his home directory 
```
su - <username>
```
### To list users of environment(machine) : 
```
cat /etc/passwd 
Tecmint :x:1000:1000:tecmint:/home/tecmint:/bin/bash
<username> :<encrypted password> : <uid>:<user’s GID>:<Comment>:<home dir >: <users shell>
```

## Linux Users - Create/Delete/Modify
### Create user - w/o password login as root 
```
user useradd <username>
```
### Create user - w/o password - as normal user with sudo 
```
sudo useradd <username>
```
### To add password to user as root user 
```
passwd <username>
```
### To add password to user as normal user - with - sudo 
```
sudo passwd <username>
```
### Create User with uid ( select 4 digit ) 
```
useradd -u <uid> <username>
```
### Create user with groupid 
```
useradd -g <group id><username>
```
### Create user with comment 
```
Useradd -c <comment> <username>
```
### Create user with home directory 
```
useradd -d <directory><username>
```
### Create user with different shell 
```
useradd -s <bin/sh> <username>
```
### Create User with all details :
```
useradd -u 1451 -g 1000 -c ggluser -d /home/ggluser -s /bin/sh ggluser
```
### Create user with expire date 
```
useradd -e 2022-10-10<username>
```
### Delete user 
```
userdel <username>
```
### Delete user with home directory 
```
userdel -r <username>
```
### Default assigned values for new user to be created 
```
useradd -D
```
### Modifying the existing user 
```
Usermod -c <comment> <username>
```
### Modify the user home directory with data 
```
usermod -d <dir> -m <username>
```
### Modify the user id and groupid 
```
usermod -u <uid> -g <gid><username>
```
### Modify username 
```
usermod -l <new name> <oldname>
```
### Modify normal user to root user(sudo group :wheel) 
```
usermod -aG wheel <username>
```
### To add group with groupid 
```
groupadd -gid 1458 <group name>
```
### To verify that group created
```
getent group | grep <groupname>
```

## Linux User File Permissions
| Filetype + users permission | Index /links | owner | user | size | date | time | File name |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| - rw-rw-r– | 1 | opc | opc | 0 | Sep 5 | 02:31 | file2 |

|  |  |  |  |
| :--- | :--- | :--- | :--- |
| File Types ( first letter ) |  - : file | d : directory | l: link |
| File Permissions | r → read (r) | w → write (w) | e → execute (x) |
| rw- rw- r– ( - means no permission) | first three for owner/admin (a) | next : group (g) | last : other users (o) |

### Add - Owner(a) + execution(x) to file 
```
chmod a+x <filename>
```
### Add - group(g) + execution(x) to file 
```
chmod g+x <filename>
```
### Add - others(o) + execution(x) to file 
```
chmod o+x <filename>
```
### Add owner,group,other + exe(x) to file 
``` 
chmod o+x,g+x,o+x <filename>
```
### Add all permission to all 
```
chmod o+rwx,g+rwx,o+rwx <filename>
```


|  |  |  |  |
| :--- | :--- | :--- | :--- |
| File Permissions | r → read (4) | w → write (2) | e → execute (1) |
| rw- rw- r– ( - means no permission) | rw- →owner : r+w+e=4+2+0=6 | rw- →group : r+w+e=4+2+0=6 | r- - →others : r+w+e=4+0+0=4 |

### Add Permissions a→rwx, g→rw, o→r ⇒ rwxrw-r--
```
chmod 764 <filename>
```
### Add Permissions a→rwx, g→rw, o→r ⇒ rwxr--r-- 
```
chmod 744 <filename>
```
### change --xr--r– ⇒ rwxr-xr-- 
```
chmod 754 <filename>
```

## Linux Filesystem Hierarchy Standard (FHS)
All the directories in the Linux system come under the root(/) directory which is represented by a forward
slash (/).

| Directory type | Types of files stored |
| :--- | :--- |
| Binary directories | Contains binary or compiled source code files, eg, /bin, /sbin, etc. |
| Configuration directories | Contains configuration files of the system, eg, /etc, /boot. |
| Data directories | Stores data files, eg, /home, /root,/media, /mnt, /tmp etc. |
| Memory directories | files which don't take up actual harddisk space, eg, /dev, /proc, /sys. |
| Usr (Unix System Resources) | Contains sharable, read only data, eg, /usr/bin, /usr/lib, etc. |
| var (variable directory) | Contains larger size data, eg, /var/log, /var/cache, etc. |
| Non-standard directories | Dir. which do not come under FHS, eg, lost+found,/run, /cdrom etc. |


## Linux - VI Editor
VI=VIsual Editor , it’s text editor in UNIX/Linux environment. It has two modes, (i) Command Mode :
based on commands you can edit text , eg: pressing dd → will delete the entire one line. (ii) Insert Mode :
whenever you enter vi (vi <filename> , by default its command mode, by pressing I you can shift into Insert
mode, here you can type , copy, paste text.
 
| | |
| :--- | :--- |
| Enter into Insert mode |  I |
| Enter back to command mode | esc |
| Move down line | j |
| Move up line | k |
| Move left | h |
| Move Right | l |
| Go to last line | G |
| Last Position | `` |
| Delete current character at cursor | x |
| Delete character before cursor | X |
| Replace current character | r |
| Delete current line | dd |
| Delete the current line from current character | D |
| Delete current line to end of the file | dG |
| undo | u |
| Repeat last command | . |
| Copy a line | yy |
| Paste after current line | p |
| Paste before current line | P |
| Join two lines | j |
| Repeat the current line | yyp |
| Move to next word | w |
| Move to back word | b |
| Delete one word | dw |
| Copy one word | yw |
| Search | / |
 
Replace all (s: string, g:globally) 
```
 :<startLine,endLine>s/<oldString>/<newString>/g → :1,$ s/one/two/ 
```
 
## Linux - Archiving
File archiving is used when one or more files need to be transmitted or stored as efficiently as possible.
 
**Archiving**: Combines multiple files into one, which eliminates the overhead in individual files and makes
the files easier to transmit.
 
**Compression**: Makes the files smaller by removing redundant information. Its two types : lossless, lossy.
 
   Lossless: No info is removed from the file. Compressing a file and decompressing= identical to the
             original.
   Lossy : Info might be removed from the file. uncompressing a file = slightly different from the
           original.
When an archive is decompressed, and one or more files are extracted, this is called **un-archiving**.
 
|  |  |  |
| :--- | :--- | :--- | 
| zip | Archive=combines files and keeps original files as it is | |
| gzip | Compress files along archive(only files) by replacing original files | Lempel-Ziv data compression |
| tar | To compress a directory | |
| bzip2 | Compress files+archive by replacing files, gen2 of gz(good compr.) | Burrows-Wheeler block sorting |
 
### zip: files+folders - combining - no compress
 
### Zip file/folder 
```
 zip <zip file name> <folder/file needs to zip> 
 zip one.zip /home/user/dir
``` 
### Unzip file/folder 
```
 Unzip <zip file name> 
 unzip <zipfile.zip>
```
### Remove file from zip 
```
 Zip -d <zipfile.zip> <files/folders to zip> 
 zip -d hii.zip hii2
```
### Add file zipped file 
```
 zip -u <zipfile.zip> <files/folders to zip> 
 zip -u hii.zip hii2-add
```
### Delete original after zip 
```
 zip -m <zipfile.zip> <files/folders to zip> 
 Zip -m one.zip/home/user/one/
```
### Recursive zip(inner folder) 
```
 zip -r <zipfile.zip> <files/folders to zip> 
 zip -r one.zip/home/user/one
```
### Exclude file 
```
 zip -x <zipfile.zip> <files/folders to exclude> 
 zip -m one.zip one.txt
```
### Verbose (info as response) 
```
 Zip -v <zipfile.zip> <files/folders to zip> 
 zip -v one.zip one.txt
```
 
### gzip (GNU (GNU’S Not Unix) zip) : files - compression at low size
 
### compress file 
```
 gzip gzip one.zip
```
### Uncompress files 
```
 gunzip <file>
 gunzip -d <File>
 
 gunzip one.zip.gz
 gzip -d one.zip.gz
```
### To see compress ratio
``` 
 gzip -l <file>
 
 gzip -l onetwo.zip
``` 
 
### bzip2 (bunzip) : compress a file like gzip command but takes a little more time but compresses better.
 
### compress file 
```
 bzip2 <files> 
 bzip all.zip
```
### Uncompress files 
```
 bzip2 -d <files> 
 bzip -x all.zip.bz2
```
 
### Tar(Tap Archive): combine+compress → files and folder → again you can add .gz and bz2 compression

|  |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| c : create | v : display output | f : mentioned destination dir. to store | z : compress with gz | j : compress with bzip2 |
 
### compress file/folder 
```
 tar -cvf <filename.tar> <files/folders> 
 
 tar -cvf all.tar *
```
### compress file/folder gz 
```
 tar -cvfz <filename.tar> <files/folders> 
 
 tar -cvfz all.tar *
```
### compress file/folder 
```
 bzip2 tar -cvfj <filename.tar> <files/folders> 
 
 tar -cvfj all.tar *
```
### To list the files in 
```
 tar -tvf <filename.tar> 
 
 tar -tvf all.tar
```
### Extract the tar 
```
 tar -xvf <filename.tar> 
 
 tar -xvf all.tar
```
 
## Linux I/O Redirection
 
Redirection can be defined as changing the way from where commands read input to where commands send
output. You can redirect input and output of a command. Using characters like > , < , >> , |
 
**standard input (stdin < )** : numbered as stdin (0). The bash shell takes input from stdin. By default
                                keyboard as i/p.
                         
**standard output (stdout > )** :numbered as stdout (1). The bash shell sends output to stdout. Output goes to
                                 display.
 
**standard error (stderr)** : numbered as stderr (2). The bash shell sends an error message to stderr - goes to
                             display
 
### > 
```
 echo “hii” > hii.txt
```
### < 
```
    run.sh < new-commands.txt
```
### >> 
```
 Network troubleshooting utility.
```

 
## Linux - Networking Commands
|  |  |
| :--- | :--- |
| ifconfig | Display and manipulate route and network interfaces. |
| ip | It is a replacement of the ifconfig command. |
| traceroute | Network troubleshooting utility. |
| tracepath | Similar to traceroute but doesn't require root privileges. |
| ping | To check connectivity between two nodes. |
| netstat | Display connection information. |
| ss | It is a replacement for netstat. |
| dig | Query DNS related information. |
| nslookup | Find DNS related query. |
| route | Shows and manipulates IP routing table. |
| host | Performs DNS lookups. |
| arp | View or add contents of the kernel's ARP table. |
| iwconfig | Used to configure wireless network interface. |
| hostname | To identify a network name. |
| curl or wget | To download a file from the internet. |
| mtr | Combines ping and tracepath into a single command. |
| whois | Will tell you about the website's whois. |
| ifplugstatus | Tells whether a cable is plugged in or not. |
 
## Linux - man
The "man" is a short term for a manual page. In unix-like operating systems such as linux, man is an
interface to view the system's reference manual.
### man <command> 
```
 Eg: man passwd → to view manual related to man command
```
### whereis <command> 
```
 To see where is manual related to than command
```
 
## Linux - System Administration Commands
|  |  |
| :--- | :--- |
| uptime | Shows how long system is on and running |
| users | Shows users - current logged in |
| free -m/g | shows storage details in m:mb , g:gb |
| last | Last users activity |
| history | Command history |
| ping | Checking the ping |
| ifconfig | Network information |
| traceroute <domain> | Tracing the domain server path |
| nslookup | Finding the server ip |
|  wget | To download via link |
| ps | List the process of current user |
| top | Processor activity of entire system including root activities |
| last | Last user activity |
| kill | To kill the process |
| jobs | To see running jobs , ex : starting sleep job : sleep 1000 & , & id run in bg |
 
 
## Linux - processes
To view currently running processes on the system with the ps command. It mostly return PID(Process ID),
TTY(type of terminal ), TIME(process cpu use time),CMD(command used)
### ps -ef 
```
 List currently running process in full format
```
### ps -ax 
```
 List current running process
```
### ps -u <username> 
```
 Listing the processes related to specific user
```
### ps -C <command> 
```
 Listing the process related to specific command
```
### ps -p <pid> 
```
 Listing the process with pid
```
### ps -ppid <ppid> 
```
 Listing with parent process id related process
```
### pstree 
```
 Shows processes in hierarchy
```
### ps -L 
```
 List all threads for a particular process
```
 
**Linux Terminating** : There are four ways to kill or terminate a process. commands allow you to run the
system uninterruptedly after terminating a process without rebooting the system. commands can be internal
or external.

|  |  |
| :--- | :--- |
| kill | To terminate a process is a kill command. You need to know the PID of the process |
| killall | It kills all the processes with the specified name in the system. |
| pkill | The pkill command uses the name of the process either by typing full name or partial name. |
| xkill | Command xkill is used to kill a process on X server without passing process name or PID |
 
## Linux - processes kill
To kill a process use command, extend with different signal numbers, command :
```
 kill -SIGNAL PID
```
Process signal names and numbers: process kill methods mentioned below,to see all signals run : kill-l
 
 
| Signal Names mostly used | Signal Number | Signal Use |
| :--- | :--- | :--- |
| SIGNULL | 0 | NULL, check access to PID |
| SIGHUP | 1 | Hangup |
| SIGINT | 2 | Interrupt |
| SIGQUIT | 3 | Quit |
| SIGKILL | 9 | Kill |
| SIGTERM | 15 | Terminate |
| SIGSTOP | 24 | Stop |
| SIGTSTP | 25 | Stop/pause the process |
| SIGCONT | 26 | Continue a stopped process |
 
|  |  |
|  :--- | :--- |
| kill -SIGNAL PID | Kill -9 1002 | Command to kill process |
| kill -SIGNAL PID | PID Kill -9 1002 1003 | Command to kill multi process |
 

## Linux - filters
Linux Filter commands accept input data from stdin (standard input) and produce output on stdout (standard
output). It transforms plain-text data into a meaningful way and can be used with pipes to perform higher
operations.
### grep 
```
 global regular expression print → filters the content of a file which makes our search easy.
 E.g : cat /etc/passwd | grep root or ls -ltr | grep videos
```
### sort 
```
 sort <fileName> , eg : sort /etc/passwd
```
 

## Linux - wget(web get)
The wget is a free non-interactive file downloader command. Non-interactive means it can work in the
background when the user is not logged in. It supports HTTP, HTTPs ,FTP protocol. Not avail install:sudo
apt-get install wget
### wget <URL> 
```
 download file
```
### wget -O <fileName> <URL> 
```
 Downloading file with altering local name to save
```
### Wget --limit-rate=<150k/speed> <URL> 
```
 To limit the speed
```
### wget -i <fileName> 
```
 Save links in text file and use that command
```
### wget -b <URL> 
```
 Download in background
```
### wget -c <URL> 
```
 Complete the remaining downloaded file s
```
### wget --tries=<Number> <URL> 
```
 Setting retry times
```
 
## Linux - Distributions
Linux Developed by many developers , associations and companies , all of them shared and developed parts
of linux. And linux open source modifying source companies releasing their distribution.
  1) RPM-based : Fedora, RedHat Linux Enterprise, CentOS, OpenSUSE, package: rpm → yum
  2) Debian-based : Ubuntu, Kali linux, parrot os , package : dpkg → apt-get or apt
  3) Arch Linux-based : Arch linux, Garuda Linux , package: pacman → pacman
 
In 1969, a team of developers of Bell Labs started a project to make a common software for all the
computers and named it 'Unix'. It was simple and elegant, used 'C' language instead of assembly language
and its code was recyclable.. As it was recyclable, a part of its code now commonly called 'kernel' was used
to develop the os.
 
In 1991, Linus Torvalds was a student at the university of Helsinki, Finland. Free version of Unix started
writing its own code. Later this project became the Linux kernel.released as GNU/Linux in 1992. It is an
open source so many companies made their modifications and released their distributions. You can see
distributions above.
 
 
## Linux - package/software installation
### RPM Package Manager: by RHEL
OS : RHEL,centos,fedora,amazon linux
YUM : Yellowdog Updater, Modified
```
yum install <package name>
E.g : Yum install tree
RHEL : rpm install <package-name>
```
###  Debian-based : by The Debian Project
OS : Ubuntu, Kali linux, parrot os
```
APT : Advanced Packaging Tool
apt-get install <package name>
E.g : apt install httpd
```
### Arch based :
OS : Arch linux, Garuda Linux
```
pacman -S <package-name>
```
 
## Linux - cronjob

To Build Job Daily or Time basic you can user cron job
 Cron Jobs has 5 values :
| Minutes | Hour |Day of Month | Month | Dow |
| :--- | :--- | :--- | :--- | :--- |
| 0-59 | 0-23 | 1-31 | 1-12 | 0-6 |
 
Task - 1: If you want to run a job every day at 10:00PM, then write cron job
Answer : 0 22 * * *
 
| Minutes | Hour | Day of Month | Month | Dow |
| :--- | :--- | :--- | :--- | :--- |
| 0 | 22 | * | * | * |
 
Task - 2 : If you want to run a job every day at 11:00 PM From Monday to Friday only,
then write cron job
Answer : 0 23 * * 1-5
 
| Minutes | Hour | Day of Month | Month | Dow |
| :--- | :--- | :--- | :--- | :--- |
| 0 | 23 | * | * | 1-5 |
 
## Examples of Cron jobs 1:
Scheduling a Job For a Specific Time The basic usage of cron is to execute a job in a specific time as
shown below. This will execute the Full backup shell script (full-backup) on 10th June 08:30 AM. The
time field uses 24 hours format. So, for 8 AM use 8, and for 8 PM use 20.
 
30 08 10 06 * /home/maverick/full-backup
 
## Elements of linux /system architecture : 
 Kernel, system library,system utility, hardware, shell and user.
 
### kernel: 
it establishes communication between user application and hardware. It stays in b/w app and
hardware. Main Functions are Memory, Storage, Device, Process management. 

#### Kernel types:
 
| Kernel | Monolithic | Micro | Hybrid |
| :--- | :--- | :--- | :--- | 
| work | services operate in kernel space | Less services@kernel, left in users | Combo of monolithic and micro |
| advtgs | Good Performance | Good stability | Good performance + stability |
| disadv. | Dependencies more | System calls are more | Dependencies more |
| os | Linux,unix and android | Blackberry, symbian, java os | Windows , MAC |
 
### Shell : 
it is a terminal environment ,here we can run our commands, it is an interface between user and kernel.
**Types** : 1) bourne shell (sh), 2) bash(Bourne-Again Shell) - bash, 3) c shell(csh), 4) korn shell(ksh), 5) z shell(zsh)

### shell scripting : 
it is like programing language, here we write shell script(commands, conditions and more) 
in file and execute, it will perform actions and process , eg: #1/bin/bash…….yum install httpd

### LILO (Linux Loader) : 
used to load Linux into memory and start the OS, simply its a boot loader.
functions such as locating kernel, identifying other supporting programs, loading memory, and starting the
kernel

### Modes of vi editor : 
i) Command mode (press ESC), (ii) Insert mode(press I), (iii) Execute mode(press :)

### Swap memory : 
Sharing the storage memory to RAM, when the RAM is used full, to handle resources/processes
 
### Daemons : 
background linux system process , that starts when os starts and ends at shutdown , no control
over it. Examples : httpd, sshd, nfsd

### Linux user mode : 
(i). CLI(Command Line Interface), (ii) GUI(Graphical User Interface)
 
###  File permissions in linux : 
(i) r - Read , (ii) w - Write , (iii). e - Execution

### Cron : 
it is program used to execute tasks at scheduled time, min time is minutes, used in servers , runs 24-7
 
### Anacron : 
execute tasks in intervals/days – mintime days – not a demon, used in Desktops and laptops, eg: updates
 
### Process ID :
