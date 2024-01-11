# Write a Shellscript to given user is root user or not

```
#!/bin/bash      
#title             :
#description       :
#author            : Mithun Technologies
#date              : 08112012
#version           : 2.0    
#usage             :
#Copy Rights       : Mithun Technologies
#Contact           : 9980923226
```

```
echo "Please enter the user name"
read userName

if [ `id -u $userName` -eq 0 ]
then
echo "Give user is root user"
else
echo "Given user is not root user"
fi
```
