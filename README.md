# <u> **Scripts** </u>


## <u>**What is bash?**</u>


1. Bash stands for Bourne Again SHell.
   
2. It is a command-line shell and scripting language.
   
3. Default shell for Unix-based operating systems like Linux and macOS.
   
4. Provides a text-based interface for interacting with the operating system.
   
5. Allows executing commands to navigate directories, run programs, manipulate files and folders, and manage system settings.
   
6. Supports scripting, enabling the creation of Bash scripts to automate tasks and perform complex operations.
   
7. Bash scripts are files containing a series of commands executed together.
   
8. Powerful tool for system administration, task automation, and small program development.


## <u>**What is a shell?**</u>


1. Software which provides an interface to run the commands.

2. A shell acts as a mediator between the user and the operating system.
   
3. It accepts commands from the user, interprets them, and communicates with the operating system to execute those commands.
   
4. The user inputs commands into the shell by typing them as text.
   
5. The shell then processes these commands and performs the requested actions, such as running programs, manipulating files, or configuring system settings.
   
6. Shells provide features like command history, command completion (auto-suggesting commands), and the ability to run commands in the background.
   
7. They often have built-in programming features, such as variables, loops, conditionals, and functions, allowing users to write scripts or automate tasks.
   
8. Shells come in different platforms, with popular ones including Bash (Bourne Again SHell), PowerShell, and Zsh.



## **<u>Navigating files and folders** </u>



````
cat command - to print out files 

ps -p <- to specify the shell you are running and process you are running.

history <- will show you list of all commands you have used

To run a command in history - find the number of the command and press !2 (number of command you need)

history --help <- This will show you more information on commands if you need help.

ls <- shows files

ls -a <- shows hidden files

![Alt text](image.png)

. <- current directory
.. <- parent directory

cd .. <- will take yo to your parent directory

cd or cd ~ <- will take you to your home directory

Not every user gets their own user folder in the home directory.

root user-super user has a special folder in the root/parent directory.

pwd <- present working directory

ls -l <- allows you to view permissions on files

ls -la <- allows you to view permission on hidden files

![Alt text](image-1.png)

(In the image - blue are directories and start with d)

Linux doesn't care about file extensions. It can recognise the type of file.

curl <- transfers data 

So in order to add a jpg - curl url

You need to print file to a specific output

curl url --output filename <- will add the jpg to the file

commands are case-sensitive!

mv filenameyouwanttochange newfilename -< This will rename the file

file nameoffile <- will tell you type of file

cp nameoffile nameofnewfile <- will copy the file

rm nameoffile <- removes file *Be careful with this command*

mkdir nameofdirectory <- creates a directory/folder

Do not use spaces in files and folders - if you have to - use "name of file" or 'name of file' or \

rm -r nameofdirectory <- This will delete all directory and files within the folder *Be careful with this command*

touch nameoffile <- will create an empty file

nano nameoffile <- Will allow you to edit your file and add content to it - press ctrl + s to save it and then ctrl + x

cat nameoffile <- to view/print file on screen

head -2 nameoffile <- Will give first two lines of the file

tail -2 nameoffile <- will give you last two lines of the file

nl nameoffile <- will number your file

