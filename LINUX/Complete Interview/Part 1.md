## 1. What is the purpose of firewall?

A firewall is a security system that controls incoming and outgoing network traffic by analyzing the data packets and determining whether they should be allowed 
through or not, based on a set of rules and security policies. The purpose of a firewall is to prevent unauthorized access to or from a private network and to 
block malicious traffic, such as malware or hackers attempting to gain access to sensitive information. Firewalls can be hardware-based, software-based, or a
combination of both. They are often used in conjunction with other security technologies, such as antivirus software, to provide multiple layers of protection for
a network.


## 2. List 3 basic commands to navigate the filesystem?

- "ls" (list) command is used to display the files and directories within the current directory. It can also be used with various options to display additional
 information about the files and directories, such as permissions and timestamps.

- "cd" (change directory) command is used to navigate to a different directory within the file system. The command takes the path of the directory as an argument.

- "pwd" (print working directory) command is used to display the current directory you are in the filesystem.

These are the most basic commands to navigate the filesystem. There are other commands such as "mkdir", "rmdir", "touch" etc. which also helps to manage the file
system but above mentioned 3 commands are basic and most commonly used.


## 3. How to check network interfaces in Linux?

There are several ways to check network interfaces in Linux, but some of the most common methods include:

- "ifconfig" command: This command is used to display information about the network interfaces on a Linux system. By running the command without any arguments, 
you will see information about all network interfaces that are currently active, including their IP addresses, netmasks, and status.

- "ip addr show" command: This command is used to display information about the IP addresses assigned to the network interfaces on a Linux system. It provides 
similar information as ifconfig, but it is considered more modern and powerful.

- "netstat" command : This command is used to display network connections and routing tables. When used with the "-i" option, it will show the network interfaces 
and their statistics, including the number of packets and bytes sent and received.

- "/sys/class/net" directory: This directory contains entries for each network interface on the system. By navigating to this directory and listing the contents, 
you can see the available interfaces.

These are the most common methods to check the network interfaces in Linux, depending on what information you are looking for, you can use the appropriate 
command to check the network interfaces.


## 4. A subnet, short for subnetwork, is a smaller network that is created by dividing a larger network into smaller, more manageable segments. This is done by 
dividing the IP address range of the larger network into smaller groups of addresses called subnets. Each subnet has its own unique IP address range, and 
devices within that range can communicate with each other directly, without the need for routing through a larger network.

For example, a network administrator can divide a Class A IP address range into smaller subnets of Class B or C IP addresses. Each subnet is then assigned a 
unique network address, and the remaining IP addresses within that range can be assigned to individual devices. This allows for more efficient use of IP addresses 
and better network management. Subnetting also improves security by isolating different segments of a network from each other, making it more difficult for 
unauthorized users to access sensitive information.


## 5. How to create a directory?

Use the "mkdir" command in the terminal to create a directory. For example, to create a directory called "myfolder" in your home directory, you would enter 
"mkdir ~/myfolder" into the terminal.


## 6. What is /bin directory used for?

The /bin directory is used to store binary executable files that are necessary for the system to boot and run single user mode. These files are commonly used by
both the system and users. Some examples of files that are typically found in the /bin directory include the ls, cp, and mv commands.

## 7. List any 3 type of filesystem?

- NTFS (New Technology File System): Developed by Microsoft, it is the default file system for Windows operating system. NTFS is a journaling file system that 
supports advanced features such as file and folder permissions, encryption, and compression.

- ext4 (Fourth Extended File System): Developed as the successor to ext3, ext4 is the default file system for Linux operating systems. It is a journaling file 
system that supports features such as extents, which improve performance and increase the maximum file size.

- FAT32 (File Allocation Table 32): Developed by Microsoft, FAT32 is a legacy file system that was commonly used on older Windows and MS-DOS systems. It does not 
support advanced features such as journaling or file permissions, but it is still widely used for removable storage devices such as USB flash drives.


## 7. What is the command to change file/directory ownership and group?

The command to change the ownership and group of a file or directory in Linux and Unix-like operating systems is "chown".
The basic syntax for the chown command is as follows:

```
chown [options] [user][:group] file
```

Where [user] is the new owner, [group] is the new group, and file is the file or directory whose ownership and group you want to change.

For example, to change the ownership of a file named "example.txt" to the user "john" and the group "users", you would run the following command:

```
chown john:users example.txt
```

You can also use chown command to change the ownership recursively with the -R option

```
chown -R john:users /path/to/directory
```

Note: you need to have superuser privilege to change the ownership of files and folders.


## 8. Can you assign one static IP to 2 computers, if not then why?

No, it is not possible to assign one static IP to two computers because each IP address is unique and is used to identify a specific device on a network. Attempting to use the same IP address on multiple devices would cause conflicts and disrupt the communication between devices on the network.


## 9. You are trying to ping a server by hostname and you get an error message, “ping: unknown host ...”.  What could be the reason and how to solve the problem so you can ping it by hostname?


There are several possible reasons why you may be getting an error message when trying to ping a server by hostname:

- DNS resolution issue: The server's hostname may not be properly configured in the DNS server, or the DNS server may be down.

- Firewall issue: A firewall may be blocking ICMP traffic, which is used by the ping command.

- Network configuration issue: The server may not be properly configured on the network, or there may be an issue with the network settings on the computer you are trying to ping from.

To solve the problem, you can try the following:

- Verify that the hostname is correct and that it is properly configured in the DNS server.

- Check the firewall settings to ensure that ICMP traffic is not being blocked.

- Check the network settings on both the server and the computer you are trying to ping from to ensure that they are properly configured.

- Try to ping the server's IP address directly instead of the hostname to see if the issue is with DNS resolution.

- If the server is on another network, check if the router is configured properly to forward the traffic to the server.

It could also be possible that the server is down or has been shut off, check with the administrator or the relevant team to confirm.


## 10. What is the name of DNS rpm package?

The name of the DNS (Domain Name System) package for the RPM (Red Hat Package Manager) package management system can vary depending on the specific Linux distribution being used.

On Red Hat Enterprise Linux, the package name is "bind" which stands for Berkeley Internet Name Domain, it is a DNS software package

On Fedora, the package name is also "bind".

You can use the command "yum search bind" to search for bind package on your system if it is a Redhat based system.

You can use the command "dnf search bind" to search for bind package on your system if it is a Fedora based system.

You can use the command "rpm -qa | grep bind" to find if the package is already installed on your system.

Please note that some other DNS server packages such as "dnsmasq" , "pdns" , "nsd" etc may also be available on Linux distributions, so you may want to check for those as well.



## 11. our company has terminated a server administrator. What is first thing as an administrator you should do to enhance the security?

The first thing an administrator should do after a server administrator has been terminated is to immediately change all relevant passwords, including any system or application-level access credentials, as well as any root or administrator-level accounts. 

It's also a good idea to review and adjust any server access controls or permissions that may have been set up by the terminated administrator. Additionally, it is important to review and monitor server logs for any suspicious activity. This can include monitoring for unusual login attempts, changes to system or application configurations, or other signs of unauthorized access. 

Finally, it is also a good practice to run a vulnerability scan on the server to identify and address any known security vulnerabilities that may exist.


## 12. What is /proc directory used for?

The /proc directory is a virtual filesystem used by the Linux kernel to store information about the system's processes, kernel parameters, and other system information. The /proc directory does not exist on disk and is generated dynamically by the kernel when the system is running. The contents of the /proc directory are organized as a set of virtual files and directories, which can be read and written to by processes running on the system.

The /proc directory contains a wide range of information about the system, including system-wide statistics, memory usage, and process-specific information. Each running process on the system has a subdirectory in /proc that contains information about that process, such as its process ID (PID), status, and other attributes.

The /proc directory also contains a number of special files that provide information about kernel parameters and other system-level information. For example, the /proc/sys/ directory contains a number of files that can be used to configure and tune various aspects of the Linux kernel, such as network settings, memory management, and security settings.

Overall, the /proc directory is an important part of the Linux operating system and provides a convenient way for system administrators and developers to access and view a wide range of system-level information and statistics.



## 13. What is the difference between memory, virtual memory and cache?

Memory, virtual memory, and cache are all types of computer storage, but they serve different purposes and have different characteristics:

- Memory (or RAM) refers to the physical memory chips that are installed in a computer. These chips hold data that the computer is currently using or processing. Memory is fast and directly accessible by the computer's CPU, but it is also volatile, meaning that it is wiped clean when the computer is powered off.

- Virtual memory is a technology that allows a computer to use hard disk space to supplement its physical memory. When the computer's physical memory is full, the system can move some of the data from memory to a special area on the hard disk called a swap file or pagefile. This allows the computer to continue running even if it runs out of physical memory. Virtual memory is slower than physical memory, but it allows the computer to run larger programs or handle more data than it could with just physical memory alone.

- Cache memory is a type of memory that is used to temporarily store frequently accessed data. The cache is typically smaller in size than main memory, but it is much faster. Cache memory is used to speed up access to frequently used data, such as instructions or data that are repeatedly used by the CPU. Caches are used at various levels of the memory hierarchy, such as the CPU cache, disk cache, and browser cache.

In summary, Memory is the physical chip that holds the data that computer is currently using, virtual memory is a technology used to supplement the physical memory with hard disk space, and cache is a small, fast memory that stores frequently accessed data to speed up access times.



## 14. Which file to edit for kernel tuning?

There are multiple files that can be edited for kernel tuning, depending on what specific settings you want to change. Some of the more commonly used files include:

- /etc/sysctl.conf: This file contains a set of sysctl parameters that can be used to configure various aspects of the Linux kernel, such as network settings, memory management, and security settings. This file can be used to change settings that are not exposed through the /proc filesystem.

- /proc/sys/kernel/: This directory contains a number of files that can be used to configure and tune various aspects of the Linux kernel, such as the maximum number of open files, maximum number of processes, and maximum size of shared memory segments.

- /proc/sys/vm/: This directory contains a number of files that can be used to configure and tune the Linux kernel's virtual memory settings, such as the maximum size of the swap file and the rate at which pages are swapped out to disk.

- /etc/security/limits.conf: This file can be used to set limits on various system resources, such as the maximum number of open files, maximum number of processes and maximum size of shared memory segments.

It is important to note that kernel tuning is a delicate task and can potentially cause instability or crashes if done improperly. It is recommended that you make a backup of the files before editing and thoroughly test the changes in a non-production environment.
Also, it is always a good idea to consult the official documentation and consult the community before making any changes.



## 15. You have scheduled a job using crontab but it does not run at the time you specified, what could be the reason and how would you troubleshoot?
There are several reasons why a cron job may not run at the specified time:

- The crontab file may contain errors or formatting issues. To troubleshoot this, check the system logs for error messages related to cron and verify the syntax of the crontab file.

- The system's time or timezone may be incorrect. Verify that the system's time and timezone are set correctly and match the schedule specified in the crontab file.

- The user's environment variables may not be set correctly. Make sure that the user running the cron job has the correct environment variables set up in their shell profile.

- The script or command specified in the crontab file may not have the necessary permissions to run. Check the permissions on the script or command and ensure that it is executable by the user running the cron job.

- The script or command specified in the crontab file may not be working correctly. Test the script or command separately to ensure that it runs correctly.

To troubleshoot, you can use the command "crontab -l" to see the current crontab entries and use "grep CRON /var/log/syslog" or "grep CRON /var/log/messages" to see the cron logs.



## 16. You noticed that one of the Linux servers has no disk space left, how would you troubleshoot that issue?
To troubleshoot a Linux server with no disk space left, you can follow these steps:

- Use the "df -h" command to check the disk usage on all file systems. This will show the percentage of disk space used and the amount of free space available.

- Use the "du -sh /*" command to check the disk usage by directory. This will show the disk space used by each directory and subdirectory.

- Identify large files or directories using the "find / -type f -size +10M" command, which will find files larger than 10MB.

- Use the "lsof +L1" command to find any deleted files that are still open by a process.

- Use the "lsof | grep deleted" command to find all deleted files that are still open by a process.

- Use the "top" command to check for any process that is taking a lot of memory and investigate it further.

- Check for files in the /tmp, /var/tmp, /var/log and /var/log/old directories that can be deleted.

- Check for files in the /var/log/apt/history.log and /var/log/apt/term.log directories that can be deleted as well

- Check for files in the /var/cache/apt/archives/ directory which can be deleted

- If you find a process or service that is using a lot of disk space, consider stopping or uninstalling it to free up space.

These are some of the common ways to troubleshoot the issue, it's important to note that the solution will depend on the specific case and what is causing the disk space to be used up.



## 17. How do you search for a pattern/word in a file and then replace it in an entire file?

There are multiple ways to search for a pattern or word in a file and replace it in the entire file, depending on the programming language and tools you are using. Here is one example of how to do this using the command line tool sed:

```
sed 's/old-pattern/new-pattern/g' input.txt > output.txt
```

This command uses the sed command to search for the string "old-pattern" in the file "input.txt" and replace it with "new-pattern", then redirects the output to a new file "output.txt". The g at the end of the command specifies that all occurrences of the pattern should be replaced, not just the first one.

Another option would be to use the find and sed command in unix/linux,

```
#python

find . -type f -exec sed -i 's/old-pattern/new-pattern/g' {} +
```

This command find all files under the current directory and execute the sed command on them to replace the pattern.

You can also use different other programming languages to achieve the same functionality, such as Python, Perl, etc.



## 18. You are notified that your server is down, list the steps you will take to troubleshoot?

When a server goes down, the first step is to determine the cause of the problem. The following are some steps that can be taken to troubleshoot the issue:

- Check the server's power supply and connections to ensure that it is properly powered on and connected to the network.

- Check the server's logs for any error messages that may indicate the cause of the problem.

- Check the server's hardware, such as the CPU, memory, and disk usage, to see if there are any issues that may be causing the server to crash.

- Check the network connectivity, ensure that the server has a valid IP address and can ping to other devices on the network.

- Check the services running on the server, if possible, restart the services that have stopped working.

- If the above steps do not resolve the issue, consider contacting the server manufacturer or a qualified technician for further assistance.

- In case the problem persist, you can also reboot the server and if it's still down, check with the hosting provider, the issue could be related to network or hardware.

- If it's a software-related issue, try to identify the process or application that is causing the problem and try to fix it or update it.

It's important to note that the troubleshooting steps may vary depending on the specific server, configuration, and the nature of the problem.


## 19. What are the different fields in /etc/passwd file?

The /etc/passwd file contains one line for each user account on a Linux or Unix-like system. Each line contains seven fields, separated by colons. The fields are as follows:

- Username: the account name of the user.

- Password: an encrypted password for the account. This field is typically set to "x" to indicate that the password is stored in the /etc/shadow file.

- User ID (UID): a unique numerical ID assigned to the user.

- Group ID (GID): the numerical ID of the user's primary group.

- User ID Info: additional information about the user, such as the user's full name or contact information.

- Home directory: the path to the user's home directory.

- Command or shell: the path to the user's default command interpreter or shell.

Note that the fields in /etc/passwd are in plain text, which is not considered secure way to store the password.



## 20. What is the file name where user password information is saved?

The file name where user password information is typically saved is called the "shadow file" and it is located in the /etc/ directory. The file is named "shadow" and it is only accessible by the root user. This file contains the hashed version of user passwords, as well as other information related to user account management.
It is important to mention that the way the password is stored depend on the system. In some system like Windows, the passwords are stored in the SAM file
