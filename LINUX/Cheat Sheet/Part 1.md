# LINUX COMMANDS

## DIRECTORY
| COMMAND  | FUNCTION  |
| :--- | :--- |
| cd | navigate through files and directories |
| cd.. | move one directory up |
| cd- | move to your previous directory |
| pwd | show the directory currently working in |
| rmdir | delete a directory and its contents |
| mkdir [directory] | create a new directory |
| scp [file_name.txt][server/tmp] | securely copy a specific file to a server directory |
| rsync -a [/your/directory][/backup/] | sychronize the contents of a specific directory with a backup directory |

## DISK USAGE
| COMMAND  | FUNCTION |
| :--- | :--- |
| df | get a report on the systems's disk space usage |
| du | check the disk space usage of a file or directory |
| fdisk -l | show disk partitions sizes and types |
| du-ah | show disk usage for all files and directory |
| du-sh | show disk usage of the current directory |
| findmint | show target mount point for all filesystems |

## FILE COMMANDS 
| COMMAND | FUNCTION |
| :--- | :--- |
| ls | list files in a directory |
| ls -R | list all files in the sub- directories |
| ls -a | list all hidden files |
| ls -al | list all files and directories with detailed information like permissions, size, owner, etc. |
| cat | list the contents of a file on standard output |
| cat>filename | creates a new file |
| diff | compare the contents of two files line by line |
| tar | archive multiple files into a common Linux |
| cat filename 1 filename 2.filename3 | joins two files (1 and 2) and stores the output in a new file |
| tax xf[compreesed_file.tar] | extract archived file |
| cat filename|tra a-z A-Z >output.txt | convert a file to upper or lowercase |
| tar czf [compressed_file.tar.gz] | create a gzip-compressed tar file |
| tar cf[compressed_file.tar][file_name] | create an archived filefrom a file |
| gzip [file_name] | compress a file with the .gz extension |
| chmod | change the read, write , and executen permissions of the files and directories | 
| chown | change or transfer file ownership |
| rm [file_name] | remove a file |
| rm -r[directory_name] | remove a directory recursively |
| rm -rf [directory_name] | remove a directory recursively without requiring confirmation |
| wc | print the number of words, lines and bytes in a file |
| cp | copy files from the current directory to a different directory |
| cp [file_name1][file_name2] |copy the contents of the first line to the second line |
| wget | downloadc the files from the internet |
| cp -r[directory_name1][directory_name2] | recursively copy the contents of the first directory into the second directory |
| mv | to move or rename files |
| mv[file_name1][file_name2] | rename file_name1 to file_name2 |
| In -s/path/to/[file_name][link_name] | create a symbolic link to afile |
| touch[file_name] | craete a new file |
| more[file_name] | show the contents of a file |
| head[file_name] | show the first 10 lines of a file |
| tail[file_name] | show the last 10 lines of a file |
| gpg -c[file_name] | encrypt a file |
| gpg[file_name.gpg] | decrypt a file |
| sudo| perform tasks that need administrative or root permissions |
| locate | to search for a file or directory |
| find | to locate files within a directory |
| jobs | display current jobs |
| kill | terminate a unresponsive program |
| history | review the commands you entered before |
|  uname | print information about Linux system |
| man | show manual instructions of Linux commands |
| zip | compress files into a zip archive |
| unzip | extract zipped files from a zip archive | 
| top | monitor system resource usage |
| ps | show a snapshoty of active processes |
| echo | move data into a file |
| hostname | know the name of your host/network |
| ping | check connectivity to a server |

## NETWORK
| COMMAND  | FUNCTION |
| :--- | :--- |
| ip addr show | show IP addresses and network interfaces |
| ipconfig | show IP addresses of all network interfaces |
| netstat-pnltu | show active ports |
| netstat-nutlp | show more information about a domain |
| whois [domain] | show more information about a domain |
| dig[domain] | show DNS information about a domain |
| host[domain] | do an IP lookup for a domain |

## SYSTEM 
| COMMAND | FUNCTION |
| :--- | :--- |
| uname -r | show system information |
| timedatectl | query and change the system clock |
| hostname -i | show the IP address of the system |
| last reboot | show system reboot history |
| date | show current time and date |
| uptime | show how long the system has been running, including load average |

## USER 
| COMMAND  | FUNCTION |
| :--- | :--- |
| id | show details of the user |
| passwd| add a password to a user's account |
| useradd | create a new user |
| last | show last logins |
| userdel [user_name] | remove a user |

## KEYBOARD SHORTCUTS 
| COMMAND | FUNCTION  |
| :--- | :--- |
| Ctrl + E | move to the end of the line |
| Ctrl + A | move to the beginning of the line |
| Ctrl + C | stop and terminate the current command |
| Ctrl + W | cut one word before the cursor and add it to the clipboard |
| Ctrl + Q | unfreeze the terminal |
| Ctrl + Z | pause the command |
| Ctrl + S | freeze the terminal |
| Ctrl + U | cut part of the line before the cursor and add it to the clipboard |
| Ctrl + K | cut part of the line after the cursor and add it to the clipboard |
| Ctrl + Y | paste from the clipbaord |
| Ctrl + R | recall the last command that matches the provided charcaters |
| Ctrl + G | exit command history without running a command |
| Ctrl + O | run the previously recalled command |
| TAB | autofill typing |
| !! | repeat the last command |
| exit | log out of the current session |
