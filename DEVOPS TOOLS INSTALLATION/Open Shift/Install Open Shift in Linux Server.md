# Install Open Shift  in Linux Server

## Login as a root user
```
sudo su -
```

## For Downloading the OC 

--------------------------------
https://mirror.openshift.com/pub/openshift-v4/clients/ocp/latest/

wget https://mirror.openshift.com/pub/openshift-v4/clients/ocp/latest/openshift-install-linux-4.7.21.tar.gz


## Extract the Package

--------------------------

tar -zxvf openshift-install-linux-4.7.21.tar.gz -O /usr/local/bin/

## Copy the package into /usr/local/bin directory

---------------------------------------------------------
 

cp -r openshift-install /usr/local/bin/

 
