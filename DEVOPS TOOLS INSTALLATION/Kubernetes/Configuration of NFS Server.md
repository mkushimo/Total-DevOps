# Configuration of NFS Server

## Step 1: Install NFS Kernel Server
Before installing the NFS Kernel server, we need to update our system’s repository index with that of the Internet 
through the following apt command as sudo:
```
$ sudo apt-get update
```
The above command lets us install the latest available version of a software through the Ubuntu repositories.

Now, run the following command in order to install the NFS Kernel Server on your system:
```
$ sudo apt install nfs-kernel-server
```
## Step 2: Create the Export Directory
```
sudo mkdir -p /mnt/share/
```
As we want all clients to access the directory, we will remove restrictive permissions.
```
sudo chown nobody:nogroup /mnt/share/
sudo chmod 777 /mnt/share/
```
## Step 3: Assign server access to client(s) through NFS export file
```
sudo vi /etc/exports

#/mnt/share/ <clientIP or Clients CIDR>(rw,sync,no_subtree_check,no_root_squash)
 #Ex:
/mnt/share/ *(rw,sync,no_subtree_check,no_root_squash)
```
## Step 4: Export the shared directory
```
$ sudo exportfs -a

sudo systemctl restart nfs-kernel-server
```
Step 5: Open firewall for the client (s) PORT 2049

# Configuring the Client Machine

## Step 1: Install NFS Common
Before installing the NFS Common application, we need to update our system’s repository index with that of the Internet 
through the following apt command as sudo:
```
$ sudo apt-get update

$ sudo apt-get install nfs-common
```
Test if we can mount nfs path with client systems folder.

## Step 2: Create a mount point for the NFS host’s shared folder
```
sudo mkdir -p /mnt/sharedfolder_client
```
## Step 3: Mount the shared directory on the client
```
sudo mount serverIP:/mnt/share/ /mnt/mountfolder_client
```
