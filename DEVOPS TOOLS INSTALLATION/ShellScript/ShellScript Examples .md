
File Name: userCreation.sh

##############################################################################################
#Purpose : This Script is to create a user and add it to devops group and set the  password.

#Author: Mithun Reddy Lacchannagari

#Date Created : June 24th 2010
##############################################################################################

clear

echo "Please enter the user name for the account you want to create!"

read userName

echo "The name you entered is: "  $userName

/usr/sbin/useradd   $userName

/usr/sbin/usermod -G devops $userName

echo ".......User is created..........."

echo ".......Now Set the password for  ....... $userName"

passwd $userName
---------------------------------------------------------------------------------------------------------------------------
File Name: createUser.sh

##############################################################################################
#Purpose : This Script is to create a user , set the  password add it into sudoers file.

#Author: Mithun Reddy Lacchannagari

#Date Created : June 24th 2010
##############################################################################################


#!/usr/bin/env bash

if [ $# -ne 1 ]
then
  echo "Usage: $0  username"
  exit
else
  USERNAME=$1
fi

# creating user
/usr/sbin/useradd $USERNAME
passwd $USERNAME

echo "User has created successfully.."
echo "Providing sudo access.."

# Giving sudo access
sed -i "/NOPASSWD/a\\$USERNAME ALL=(ALL)       NOPASSWD: ALL" /etc/sudoers

echo "Sudo access provided successfully.."
