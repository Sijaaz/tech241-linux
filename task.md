**What command changes file permissions?**

First one is changing files in the numeric mode.
Second is the symbolic mode where you put enter user class and the permissions you want to grant them.

```
$ chmod 744
$ chmod ug+rwx example.txt
$ chmod o+r example2.txt
```

The u - represents permissions for the user owner

The g - represents other users in the files group

The o - represents other users not in the files group

r - read

w - write

e - execute

Plus sign to add
Minus sign to remove

**To change permissions on a file what must the end user be? (2 answers)**

Only owner and admin can change permissions on the file.

Owner of the file can use chwown or chgrp to change the ownership of a file.


**Give examples of some different ways/syntaxes to set permissions on a new file (named testfile.txt) to:**

```
chmod ug+rwx testfile.txt
```

```
chmod 744 testfile.txt
 ```

chmod ug-rwx testfile.text - will grant owner read, write and execute to owner and group.

Chmod 744 - will grant read, write and execute permissions for owner and read permission for group.


**Set User to read, Group to read + write + execute, and Other to read and write only**

```
chmod u=r,g=rwe,o=rw testfile.txt

```

**Add execute permissions (to all entities)**

```
chmod ugo=e textfile.txt
```

**Take write permissions away from Group**

```
chmod g-w testfile.txt
```



**Use numeric values to give read + write access to User, read access to Group, and no access to Other.**

```
chmod 640 testfile.txt
```

Octal values

The first digit is for owner permissons
The second digit is for group permissions.
The third digit is for other users.

r - 4 (read)
w - 2 (write)
x - 1 (execute)

https://developers.redhat.com/cheat-sheets/linux-commands-cheat-sheet-old?intcmp=701f20000012ngPAAQ

https://www.redhat.com/sysadmin/linux-file-permissions-explained