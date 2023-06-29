
# <u> **The difference between using & and nohup** </u>


If you run node app.js & - this will run the app in the background however you can't start the app again.

if you run nohup node app.js & - This allows you to run the app in the background and start and stop app when needed.

The main difference between node app.js & and nohup node app.js & lies in how they handle the application's output and the application's behavior when the terminal session ends.


**The node app.js & command**

This command runs the node app.js command in the background, allowing you to continue using the terminal. However, the application's output, including any error messages or console logs, will still be displayed in the terminal. If you close the terminal session or terminate the shell, the application will be terminated as well.

**The nohup node app.js & command**

The nohup command is used to prevent the application from being terminated when the terminal session ends. It detaches the application from the current terminal, allowing it to keep running even if the terminal is closed. Additionally, nohup redirects the application's output to a file named nohup.out by default, so the application's output will not be displayed in the terminal. This is useful for long-running processes that you want to keep running even after logging out. If you need to check the output, you can examine the nohup.out file.

In summary, nohup node app.js & provides the additional benefit of keeping the application running even after the terminal session ends and redirecting the output to a file, while node app.js & simply runs the application in the background without those extra features.

# **<u>Blockers whilst trying to connect both App and Database</u>**

- IP address wasn't working because HTTP rule was blocked on my app Virtual Machine.
- Had to make a new inbound rule on app virtual machine - which allowed HTTP.
- This opened up my IP address and allowed it to work.
- Make sure to run the database script first and then run the app script second

# **<u>To manually set nginx reverse proxy</u>**

Step 1.

sudo nano /etc/nginx/sites-available/default

Step 2.

proxy_pass http://localhost:3000;

Step 3. 

sudo systemctl restart nginx
