
The package management is a method of installing,updating,removing software on the system.

In RedHat Linux Distribution we can use yum command for installing, updating and removing the software.

Note: yum command need to execute as a root user or with sudo access.

Install a Package with YUM

To install a package any, use below command syntax.

Syntax: yum install <<package name>>
Example: yum install tree

The above command will ask confirmation before installing any package on your system. If you want to install packages automatically without asking any confirmation, use option -y as shown in below example.

Syntax: yum install <<package name>> -y
Example: yum install vim -y
We can install multiple packages with separated by space for each package name as follows.

#yum install zip unzip tar -y

Updating a Package using YUM
Using yum command we can update the package as follows.

Syntax: yum update <<package name>> -y
Example: yum update tree -y

UN-Install /Remove a Package using YUM
Using yum command we can uninstall the package as follows.

Syntax: yum remove <<package name>> -y
Example: yum remove tree -y

Get Information of a Package using YUM
Using yum command we can get the package information as follows.

Syntax: yum info <<package name>>
Example: yum info tree

List all Available Packages using YUM

To display all the package which are available in yum repository, use the below command.

#yum list

List all Installed Packages using YUM

To display all the package which are installed in Linux server, use the below command.

#yum list installed

Check for Available Updates using Yum

To find how many of installed packages on your system have updates available, to check use the following command.

#yum check-update

Update System using Yum

To keep your system up-to-date with all package updates, run the following command. It will install all latest patches and security updates to your system.

#yum update

List all available Group Packages

In Linux, number of packages are bundled to particular group. Instead of installing individual packages with yum, you can install particular group that will install all the related packages that belongs to the group. For example to list all the available groups, just issue following command.

#yum grouplist

Install a Group Packages

To install a particular package group, we use option  groupinstall as follows.

#yum groupinstall 'Development Tools'

To know how many packages are available in particular group, execute the below command.

#yum groupinfo 'Development Tools': Here Development Tools is a group name.

Update a Group Packages

To update any existing installed group packages, just run the following command as shown below.

#yum groupupdate 'Development Tools'

Remove a Group Packages

To delete or remove any existing installed group from the system, just use below command.

#yum groupremove 'Development Tools'

