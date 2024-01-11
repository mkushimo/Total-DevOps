# LINUX COMMANDS CHEAT SHEET 

## SYSTEM
| command | function  |
| :--- | :--- |
| uname | displays Linux system information |
| uname-r | displays kernel release information |
| uptime | displays how long the system has been running including load average |
| hostname | shows the system hostname |
| hostname -l | displays IP address of the system |
| last reboot | shows system reboot history |
| date | displays current system date and time |
| timedated | query and change the system clock |
| cal | sisplays the current calendar month and day |
| w | displays currently logged in users in the system |
| whoami | displays who you are logged in |
| finger username | displays information about the user |

## HARDWARE
| COMMAND  | FUNCTION  |
| :--- | :--- |
| dsmesg | displays bootup messages |
| cat/proc/cpuinfo | displays more information about CPU e.g model, model name, cores, vendor id. |
| cat/proc/meminfo | displays more information about hardware memory e.g total and free memory |
| ishw | displays information and system's hardware and configuration |
| isbik | displays block devices related information |
| free -m | displays free and used memory in the system (-m flag indicates memory in MB) |
| ispci -tv | displays PCI devices in a tree-like diagram |
| isusb -tv | displays USB devices in a tree-like diagram |
| dmidecode | displays hardware information from the BIOS |
| hdparm -i /dev/xda | displays information about disk data |
| hdparm -lt/dev/xda | conducts a read speed test on device data |
| badblocks -s/dev/xda | tests for unreadable blocks on disk |

## USERS
| COMMAND  | FUNCTION  |
| :--- | :--- |
| id | displays the details of the active user eg. uid, gid and groups. |
| last | shows the last logins in the system |
| who | shows who is in logged in to the system |
| groupadd 'admin' | adds the group 'Admin' |
| adduser 'Sam' | Adds user Sam |
| userdel 'Sam' | deletes user Sam |
| usermod | used for changing/modifying user information |

## FILE COMMANDS
| COMMAND  | FUNCTION  |
| :--- | :--- |
| ls -al | Lista files- both regular and hidden files and their permissions as well |
| pwd | displays the current directory file path |
| mkdir 'directory_name | creates a new dictionary |
| rm file_name | removes a file |
| rm -f filename | forcefully removes a file |
| rm -r directory_name | removes a directory recursively |
| rm -rf directory_name | removes a directory forcefully and recursively |
| cp file1 file2 | copies the contents of file1 to file2 |
| cp -f dir1 dir2 | recursively copies dir1 to dir2. dir2 is created if it does not exist |
| mv file1 file2 | renames file1 to file2 |
| ln -s/path/tofile_name link_name | creates a symbolic link to file_name |
| touch file_name | creates a new file |
| cat >file_name | places standard input into a file |
| more file_name | ouputs the contents of a file |
| head file_name | displays the first 10 lines of a file |
| tail file_name | displays the last 10 lines of a file |
| gpg -c file_name | encrypts a file |
| gpg file_name.gpg | decrypts a file |
| wc | prints the number of bytes, words and lines in a file |
| xargs | executes commands from standard output |

## PROCESS RELATED
| COMMAND  | FUNCTION  |
| :--- | :--- |
| ps | displys currently active processes |
| ps aux|grep 'teinet' | searches for the id of the process 'teinet' |
| pmap | displays memory map of processes |
| top | displays all running processes |
| kill pid | terminates process with a given pid |
| killall proc | kills/terminates all processes named proc |
| pkill process-name | sends a signal to a process with its name |
| bg | resumes suspended jobs in the background |
| fg | brings suspended jobs to the foreground |
| fg n | brings jobs n to the foreground |
| isof | list files that are open by processes |
| renice 19 PID | makes a process run with very low priority |
| pgrep firefox | find firefox process ID |
| pstree | visualizing processes in tree model |


## FILE PERMISSION 
| COMMAND  | FUNCTION  |
| :--- | :--- |
| chmod octal filename | change file permissions of the file to octal |
| chmod 777/data/test c | set rwx permissions to owner, group and everyone (everyone else who has access to the server |
| chmod 755/data/test c | set rwx to the owner and r_x to the fropu and everyone |
| chmod 766/data/test c | sets rwx for owner, rw for group and everyone |
| chown owner user-file | change ownership of the file |
| chown owner-user.owner-group file_name | change owner and group owner of the file |
| chown owner-user.owner-group-directory | change owner and group owner of the directory |

## NETWORK
| COMMAND  | FUNCTION  |
| :--- | :--- |
| ip addr show | displays IP addresses and and all the network interfaces |
| ip address and 192.168.0.1/24 dev ethO | assigns IP address 192.168.0.1 to interface ethO |
| ifconfig | displays IP addresses of all network interdfaces |
| ping host | ping command sends an ICMP echo request to establish a connection to server/PC |
| whois domain | retrieves more information about a domain name |
| dg domain | retrieves DNS information about the domain |
| dg -x host | performs reverse lookup on a domain |
| host google.com | performs an IP lookup for the doamin name |
| hostname -l | displays local IP addresses |
| wget file_name | downloads a file from an online source |
| nestat -pnitu | displys all active listening ports |

## COMPRESSION/ARCHIVES 
| COMMAND  | FUNCTION  |
| :--- | :--- |
| tar -cf home.tar home | creates archive file called 'home.tar' from file 'home' |
| tar -xf files.tar | extract archive file 'file.tar' |
| tar.zcvfhome.tar.gz source-folder | creates gzipped tar archive file from source folder |
| gzip file | compression a file with gz.extension |

## INSTALL PACKAGES
| COMMAND  | FUNCTION  |
| :--- | :--- |
| rpm -i pkg_name.rpm | install an rpm package |
| rpm -e pkg_name | removes an rpm package |
| dnf install pkg_name | install package using dnf utility |

## INSTALL SOURCE (COMPILATION) 
```
/configure
make 
make install 
```

## SEARCH 
| COMMAND  | FUNCTION  |
| :--- | :--- |
| grep 'pattern' files | search for a given pattern in files |
| grep -r pattern dir | search recursively for a pattern in a given directory |
| locate file | find all instances of the file |
| find/home/-name'index | find file names that begin with 'index' in home. folder |
| find/ home -size -10000k | find files greater than 10000k in the home folder |

## LOGIN 
| COMMAND  | FUNCTION  |
| :--- | :--- |
| ssh user@host |securely connect to host as user |
| ssh -p port_number user@host | securely connect to host using a specified port |
| ssh host | securely connect to the system via SSH default port 22 |
| teinet host | connect to host via teinet default port 23 |

## FILE TRANSFER 
| COMMAND  | FUNCTION  |
| :--- | :--- |
| scp file 1.txt server2/tmp | securely copy file1 txt to server2 in /tmp directory |
| rsync -a/home/apps/backup/ | sychronize contents inn /home/apps directory with /backup directory |

## DISK USAGE 
| COMMAND  | FUNCTION  |
| :--- | :--- |
| df -h | displays free space on mounted systems |
| df -i | shows free inodes on file systems |
| fdisk -i | shows disk partitions, sizes and types |
| du-sh | displays disk usage in the current directory in a human-readable format |
| fndmnt | displays target mount point for all filesystems |
| mount device-path mount-point | Mount a device |

## DIRECTORY TRAVERSE
| COMMAND  | FUNCTION  |
| :--- | :--- |
| cd_ | move up one level in the directory tree structure |
| cd | change directory to $HOME directory |
| cd/test | change directory to /test directory |

