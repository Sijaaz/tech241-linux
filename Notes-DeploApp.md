# **Deploying the app - Instructions**

```
Step 1. Update and upgrade first 

Step 2. Install nginx 

Step 3. Make sure git is installed

Step 4. Install node js

Step 5. (To install js -> curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash - )

Step 6. sudo apt install nodejs -y

Step 7. sudo nmp install pm2 -g (pm2 is to run js node in the background)

Step 8. cd (go into the actual app file) 

Step 9. npm install

Step 10. To check if nginx is running - copy paste the public ISP on the broswer

Step 11. npm start or node app.js (to start the app)

Step 12. To check if app is running - paste public isp with :3000 (To go to the port - the port is a sepcific room to the house, like a storeroom (to reach a particular server)

Step 13. Go to Azure - networking -

Add inbound port rule 

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
```
<u> **Troubleshooting** </u>

To close the app - better to use control C 

- Control z can crash the app - which may lead to using kill commands 
if this happens:
- ps aux or ps - find the PID
- kill PID
- 
# **Manually deploy database**

Step 1. To manually deploy database - create a new virtual machine for database. 

Step 2. To change subnet on Virtual Network --> Go to Overview of VM Database -> Network interface -> IP configurations
(Change subnet to default)

Step 4. SSH into this new VM with private key.

**Requirements to run Database VM**

- Ubuntu 18:04
  
- Update and Upgrade Linux

- Install mongo db 3.2.x (non relational data base - stores information as documents)
  
(Download the key for the right version) - from the mongo website - instructions there.)

- Source list - specify the mongo db version 
  
```
Step 1. wget -qO - https://www.mongodb.org/static/pgp/server-3.2.asc | sudo apt-key add -

Step 2. echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list 
```

Step 3. Run update command again
  
Step 4. Command to install
  
```  
Step 5. sudo apt-get install -y mongodb-org=3.2.20 mongodb-org-server=3.2.20 mongodb-org-shell=3.2.20 mongodb-org-mongos=3.2.20 mongodb-org-tools=3.2.20

Step 6. sudo nano /etc/mongod.conf
```
Step 7. Change - bindIP - 0.0.0.0 <- to allow any machine - security hole only allowed for testing.

Step 8. To check if bindIP has been changed correctly
```
 cat /etc/nameoffile
 ```
Step 9. Start mongo db

sudo systemctl start mongod
  
Step 10. Enable mongo db

sudo systemctl enable mongod

To check

Step 11. sudo systemctl status mongod
  


# **To connect VM app to VM Database**

Step 1. Open two gitbash terminals - one for app and one for database.

Step 2. Go to DB Virtual Machine on Azure

Step 3. Go to Networking and
add Inbound security rule

Destination - ANY

Service - CUSTOM

Destination Port ranges - 27017

Protocol - TCP

Action - Allow

Priority - 310

Name - No changes

Description - For Mongo DB


Set a environmental variable - so that app can look up the value (This will specify IP address and port of the database)

Step 4. Go to app folder
```
export DB_HOST=mongodb://<IP-ADDRESS>:27017/posts

Step 5. export DB_HOST=mongodb://51.142.195.122:27017/posts

Enter the IP address of DB 

```
This will create a DB_HOST environment variable.

**To check environment variable:**

```
printenv DB_HOST
```
```
npm install
```

```
npm start
```

**To check on webpage:**

IP address:3000/posts

