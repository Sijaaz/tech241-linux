![Alt text](Task1.png)

#!/bin/bash

Step 1 - Update

sudo apt update -y

Step 2 - Upgrade

sudo apt upgrade -y

Step 3 - Install nginx

sudo apt install nginx -y

Step 4 - Restart nginx

sudo systemctl restart nginx

Step 5 - enable nginx - will auto start on reboot

sudo systemctl enable nginx

Step 6 - Install nodejs - part a

curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

Step 7 - Install nodejs - part b

sudo apt install nodejs -y

Step 8 - Install nodejs - part c

sudo npm install pm2 -g

Step 9 - Copy app folder to VM

git clone https://github.com/jungjinggg/tech241_sparta_app.git app2

Step 10 - Cd into app folder

cd /home/adminuser/app/app

Step 11 - Install npm

npm install

Step 12 - Run Sparta app in the background

pm2 start app.js
