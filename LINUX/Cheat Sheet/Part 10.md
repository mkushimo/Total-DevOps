# LINUX COMMANDS CHEAT SHEET

## System Information Commands
|   |   |
| :--- | :--- |
| uname -a | shows Linux system info |
| uname -r | shows kernel release info |
| cat /etc/redhat-release | shows installed redhat version |
| uptime | displays system running/life time |
| hostname | shows system host name |
| hostname -I | shows ip addresses of the host |
| last reboot | displays system reboot history |
| date | displays current date and time |
| cal | displays monthly calendar |
| mount | shows mounted filesy-stems |

## File Commands
|   |   |
| :--- | :--- |
| ls -l | shows file type and access permission |
| ls -a | lists also hidden files |
| ls -al | lists files and directories detailly | 
| pwd | shows present directory | 
| mkdir directory |  creates a directory | 
| rm xyz | deletes file xyz | 
| rm -r /xyz | deletes directory /xyz and its contents recursively | 
| rm -f abc | forcefully deletes abc file without confirmation | 
| rm -rf /xyz | forcefully deletes directory /xyz recursively | 
| cp aaa bbb | copies aaa file to bbb file  | 
| cp -r /xxx /yyy | copies /xxx directıry to /yyy directory | 
| mv aaa bbb | renames or moves file aaa to file bbb  | 
| touch abc | creates an empty file named abc | 
| cat abc | used to view file abc | 
| less abc | browse through a text file abc  | 
| head abc | displays first 10 lines of file abc | 
| tail abc | displays last 10 lines of file abc | 
| tail -f abc | displays last 10 lines of file abc and follow it as it grows | 
| tail -F abc | outputs last lines of abc as it changes | 
| file abc | gets type of abc | 
| gpg -c abc | encrypts file abc  | 
| gpg abc | decrypts file abc  | 
| dir | shows files in the current directory | 
| put abc | uploads file ‘abc’ from local to remote device | 
| get file | downloads file ‘abc’ from remote to local device |

## User Information Commands
|   |   |
| :--- | :--- |
| id | shows user&group ids of the current user | 
| last | shows the last users logged on | 
| whoami | shows who you are logged in as | 
| who | shows who is logged into the system | 
| w | shows who is logged in and what they do | 
| groupadd test | creates group “test”  | 
| useradd -c “GK” -m Gokhan | creates “Gokhan” account with comment “GK” | 
| userdel Gokhan | deletes account “Gokhan” | 
| usermod -aG Networkers Gokhan | adds account “Gokhan” to the “Networkers” group | 

## File permissions
### chown user 
```
changes ownership of a file/directory
```
### chown user:group filename 
```
changes user and group for a file or directory
```
### File Permissions
```
r (read) permission, 4
w (write) permission, 2
x (execute) permission, 1
-= no permission
```
### File Owner
```
owner/group/everyone
```
### File Permissions Examples
```
777 | Owner, Group, Everyone has rwx permissions
744 | Owner has rwx permission, Group, Everyone has r permission
755 | Owner has rwx permission, Group, Everyone has rx permissions
776 | Owner, Group has rwx permission, Everyone has rw
```

## Search Commands
|   |   |
| :--- | :--- |
| grep x file | searches for x in file | 
| grep -i | case insens-itive search  | 
| grep -r | recursive search | 
| grep -v | inverted search | 
| grep -o | shows only matched part of the file | 
| find /dir/ -name aaa* | finds files starting with aaa in dir | 
| find /dir/ -user Gokhan | finds files owned by Gokhan in dir | 
| find /dir/ -mmin 10 | finds files modifed less than 10 minutes ago in dir | 
| find /home -size +500M | finds files larger than 500MB in /xyz | 
| find [/folder/location] -name [x] | finds file names starting with character x | 
| whereis aaa | locates the binary, source, and manual page of aaa | 
| locate abc | finds the location of abc quickly | 

## ls Options
|   |   |
| :--- | :--- |
| -a | shows all (including hidden)  | 
| -R | recursive list | 
| -r | reverse order | 
| -t | sort by last modified | 
| -S | sort by file size | 
| -l | long listing format | 
| -1 | one file per line | 
| -m | comma--sep-arated output | 
| -Q | quoted output | 

## Process Management Commands
|   |   |
| :--- | :--- |
| ps | displays currently running processes | 
| ps PID | gives the status of a particular process | 
| pidof | gives the process ID of a process  | 
| ps -ef | displays all running processes on the system | 
| ps -ef | grep xyz | displays process information for xyz | 
| top | displays and manages the top processes  | 
| htop | interactive process viewer (top alternative) | 
| kill pid | kills process with process ID of pid | 
| pkill xyz | kills process with name xyz | 
| killall abc | kills all processes named abc | 
| program & | starts program in the background | 
| bg | lists and resumes stopped jobs in the background | 
| fg | brings the most recent background job to foreground. | 
| fg x | brings job x to the foreground | 
| nice | starts a process with a given priority | 
| renice | changes priority of an already running process | 
| pstree | displays processes in a tree-like diagram | 
| pmap | displays a memory usage map of processes | 
| lsof | lists files opened by running processes | 

## Search commands
|   |   |
| :--- | :--- |
| command -h / command–help | to review all available options of the “command” | 
| info command | to find info documents about the “command”  | 
| whatis command | displays a single line description about the”command”  | 
| $ man UNIXCOMMAND | to view detailed man page of the “command” | 
| apropos | used to search man pages for available commands on a specific | 

## File Transfer Commands
|   |   |
| :--- | :--- |
| scp file.txt server:/tmp | secure copy file.txt to the /tmp folder on server | 
| scp server:/var/www/*.html/tmp | secure copy *.html files in /var/www/ directory on server to |
| scp server:/var/www/*.html /tmp | secure copy *.html files in /var/www/ directory on server to |
| rsync -a /home /backups/ | synchronize /home to /backups/ |
| rsync -avz /home server:/backups/ | Synchronize files/directories between the local and remote |

## Disk Usage Commands
|   |   |
| :--- | :--- |
| df | shows free hard disk space on the system|
| df -h | shows free and used space on mounted filesystems |
| df -i | shows free and used inodes on mounted filesystems |
| fdisk -l | shows free and used inodes on mounted filesystems |
| du -sh | shows total disk usage off the current directory |
| du -ah | shows disk usage for all files and directories in readable format |
| free | shows free RAM on the system |
| free -h | shows free and used memory |
| findmnt | shows target mount point for all filesystem |
| mount /xyz /abc | mounts a device in /xyz to /abc |

## Compress and Decompress Commands
|   |   |
| :--- | :--- |
| gzip abc | compresses abc file using gzip. |
| bzip2 abc | compresses abc file using bzip2 |
| zip abc.zip abc | compresses abc file into the archive abc.zip. |
| tar -czvf archive.tar.gz /home/temp2/ | compresses a full directory with all subdirectories |
| gzip -d xyz.gz | extracts xyz.gz with gzip utility |
| gunzip xyz.gz | extracts xyz.gz with gzip utility |
| bzip2 -d file.php.bz2 | extracts xyz.gz with bzip2 utility |
| bunzip2 file.php.bz2 | extracts xyz.gz with bzip2 utility |
| unzip xyz.zip | extracts xyz.zip with zip utilit |
| gunzip -c output.txt.gz | to view the contents of both files without extracting |
| tar cf archive.tar directory | creates tar named archive.tar containing directory |
| tar xf archive.tar | extracts the contents from archive.tar |
| tar czf archive.tar.gz directory | creates a gzip compressed tar file name archive.tar.gz |
| tar xzf archive.tar.gz | extracts a gzip compressed tar file |
| tar cjf archive.tar.bz2 directory | creates a tar file with bzip2 compression |
| tar xjf archive.tar.bz2 | extracts a bzip2 compressed tar file |

## Networking Commands
|   |   |
| :--- | :--- |
| arp | displays ARP table of the device |
| arpwatch | displays ethernet activity and Ethernet/ip pairings  |
| bmon | displays bandwidth, captures |
| curl | used for for file transfer |
| dhclient | used to analyze clients ip address, subnet mask, gateway, dns server |
| dig | used for simple DNS lookup |
| dstat | collects and shows system resources |
| ethtool | used to check settings of your NIC |
| ftp | used for for file transfer |
| host | used for IP-Name matchings |
| hping3 | used for packet analyze |
| ifstat | used to monitor network interface statistics |
| ip addr | used to check network interfaces and routing activities |
| iptables | used for ip packet filtering |
| iftop | displays current bandwidth usage |
| ifup/ifdown | used to enable or disable interfaces |
| iwconfig | used to configure wireless interfaces |
| netstat | to check network connections |
| nload | used as bandwidth monitoring tool |
| nmap | used for security audits |
| nslookup | used also for DNS query |
| ping | used to check reachability |
| route | displays IP Routing Table |
| scp | secured file transfer |
| sftp | secured file transfer |
| ss | gives detailed information about the sockets |
| ssh | used for secure connection |
| tshark | analyzing and capturing |
| tcpdump | used for analyzing and capturing |
| telnet | used for classical unsecure connection |
| tshark | used for packet analyze |
| tracepath | used for path tracking |
| traceroute | used for path tracking |
| w | used to check the current system activity |
| wget | used to download the content of the web servers |
| whois | checks the whois database and return with IP and Domain info |

## Install Commands
|   |   |
| :--- | :--- |
| yum search keyword | compresses abc file using gzip. |
| yum install abc | installs abc package |
| yum info abc | displays description and summary info about abc package  |
| rpm -i abc.rpm | installs package from local file named abc.rpm |
| yum remove abc | Remove/uninstall abc package |
| yum list installedl | lists all installed packages with yum |
| yum search [keyword] | finds a package by a related keyword |
| yum info [package_name] | shows package information and summary |
| yum install [package_name.rpm] | installs a package using the YUM package manager |
| dnf install [package_name.rpm] |installs a package using the DNF package manager |
| apt-get install [package_name] | installs a package using the APT package manager |
| rpm -i [package_name.rpm] | installs an .rpm package from a local file |
| rpm -e [package_name.rpm] | removes an .rpm package |

## Hardware Information Commands
|   |   |
| :--- | :--- |
| dmesg | displays messages in kernel ring buffer |
| cat /proc/cpuinfo | displays CPU information |
| cat /proc/meminfo | displays memory information |
| lspci -tv | displays PCI devices |
| lsusb -tv | displays USB devices |
| dmidecode | displays DMI/SMBIOS from BIOS |
| hdparm -i /dev/sda | displays info about disk sda |
| hdparm -tT /dev/sda | performs a read speed test on disk sd |
| badblocks -s /dev/sda | tests for unreadable blocks on disk sda |
