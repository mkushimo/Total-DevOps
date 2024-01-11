# Step 1
- To convert .pem file to .ppk , we need to use the puttygen software.
- Download the puttygen(for 64 bit Windows OS) software by using below url.
```
https://the.earth.li/~sgtatham/putty/latest/w64/puttygen.exe
```

# Step 2 
- Open the puttygen software.
- Click on puttygen.exe icon.
- Once you have double clicked on puttygen.exe file, it will open the below screenshot.

 
# Step 3 
- Load the pem file as follows.
- Click on Load button and select the pem file and click on Open, as follows.
- Once you have clicked on Open, you will see below popup, click on OK button.

# Step 4
- Save the ppk file.
- Click on Save private key button and select the path to store the ppk file as follows.
- Give the filename for ppk file and click on Save button as follows.
- Click on close symbol, once you have successfully generated.

# Step 5 
- Login into AWS EC2 instance  using ppk file as follows.
- Download the putty software (for 64 bit Windows OS) from below url if you don’t have downloaded already from below url.
```
https://the.earth.li/~sgtatham/putty/latest/w64/putty.exe
```
- Once you have downloaded the putty software copy the putty software executable file (putty.exe) from Downloads folder to Desktop.
- Open the Putty software. (Double click on putty.exe file), as follows.
- Give the IP address of which server you want to connect as follows.

## Select the ppk file
- Expand on SSH --> Expand Auth --> Click on Browse and select the ppk file and click on Open button as follows.
- Give the username as ec2-user for RHEL instance and hit the Enter button.
- Type exit command for disconnecting.
