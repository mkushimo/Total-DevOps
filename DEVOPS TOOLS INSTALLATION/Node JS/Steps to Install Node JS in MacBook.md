# Steps to Install Node JS in MacBook
 
## Download the nvm install script via cURL, install NVM package with below command.
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
``` 
## Check NVM installed successfully and which version of NVM using below command.
```
nvm --version
```
## Install the latest version of Nod Js with below command. 
```
nvm install node
```
## Use the latest version of Node JS
```
nvm use node
```
## Install the latest LTS version of Node JS
```
nvm install --lts
```
## Use the latest LTS verison of Node JS
```
nvm use --lts
```
## Install the v10.17.0 version of Node JS
```
nvm install v10.17.0`
```
## Use the  v10.17.0 verison of Node JS
```
nvm use  v10.17.0
```
## Run app.js using node v0.10.32 
```
nvm run 0.10.32 app.js    
```
## Set default node version on a shell  
```
nvm alias default 0.10.32                     
```
## Uninstall NVM
```
To remove, delete, or uninstall nvm - just remove the `$NVM_DIR` folder (usually `~/.nvm`)
```
