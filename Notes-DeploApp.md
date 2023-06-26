
**Deploying the app - Instructions**


- Update and upgrade first 
- Install nginx 
- m=Make sure git is installed
- Install node js

```
(To install js -> curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash - )

- sudo apt install nodejs -y

- sudo nmp install pm2 -g (pm2 is to run js node in the background)

- cd (go into the actual app file) 

- npm install

- To check if nginx is running - copy paste the public ISP on the broswer

- npm start or node app.js (to start the app)

- To check if app is running - paste public isp with :3000 (To go to the port - the port is a sepcific room to the house, like a storeroom (to reach a particular server)

- Go to Azure - networking - Add inbound port rule 

- Click inbound port rule - 
- Source - Any
- Source Port Ranges *
- Destination - Any
- Service - Custom
- Destination - 3000
- Protocol - TCP
- Action - Allow
- Priority - 330 (Lower the priority the higher a priority a rule has)
- Name 
- Description - For sparta app

- Two services cannot use the same port**

- **Troubleshooting**

To close the app - better to use control C 

- Control z can crash the app - which may lead to using kill commands 
if this happens:
- ps aux or ps - find the PID
- kill PID
```

To manually deploy database - create a new virtual machine for database. 

To change subnet on Virtual Network

--> Overview -> Network interface -> IP configurations

- SSH into this new VM with private key.

**Requirements to run Database VM**

- Ubuntu 18:04
  
- Update and Upgrade Linux

- Install mongo db 3.2.x (non relational data base - stores information as documents)
  
(Download the key for the right version) - from the mongo website - instructions there.)

- Source list - specify the mongo db version 
  
```
wget -qO - https://www.mongodb.org/static/pgp/server-3.2.asc | sudo apt-key add -

echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list 
```

- Run update command again
  
- Command to install
  
```  
sudo apt-get install -y mongodb-org=3.2.20 mongodb-org-server=3.2.20 mongodb-org-shell=3.2.20 mongodb-org-mongos=3.2.20 mongodb-org-tools=3.2.20

sudo nano /etc/mongod.conf
```
Change - bindIP - 0.0.0.0 <- to allow any machine - security hole only allowed for testing.

To check if bindIP has been changed correctly
```
 cat /etc/nameoffile
 ```
- Start mongo db
  
- Enable mongo db
  
- Configure mongo db to accept connections from any app VM.

