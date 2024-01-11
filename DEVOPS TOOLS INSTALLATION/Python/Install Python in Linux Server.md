# Install Python in Linux Server

- Login as a root user
```
sudo su -
```

- Install the development group
```
yum groupinstall development -y

yum install wget tar -y
cd /opt

wget https://www.python.org/ftp/python/3.9.5/Python-3.9.5.tgz

tar -xvf Python-3.9.5.tgz

cd Python-3.9.5
./configure

sudo  make install

python3 --version

python --version
```

- Install PIP

PIP is a package manager for Python packages, or modules if you like. Note: If you have Python version 3.4 or later, PIP is included by default.

- Download the PIP file
```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```

- Install PIP by using the below command
```
python3 get-pip.py
``` 

- Check the PIP version
```
pip3 --version 
```
