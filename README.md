**File Permissions:**
Understanding the permission bits of a file:
d | rwx | r-x | r-x 
The first bit tells is it a directory (d)
the next 3 bits tells about the user permissions read(r), write(w), executable(x)
the next 3 bits tells about the userGroup permissions
the next 3 bits tells about the other permissions

**Modidfying permissions:**
We use the chmod command to give or take away the permisssions with + or -
chmod u+x filename gives the user executable permissions to the user
we can also modify the permissions using the numerical format
4 - read, 2 - write, 1- execute
chmod 755 mfile 
7 : 4+2+1 for user all the permissions
5 : 4+1 for usergroup granting r and x permissions
5 : 4+1 for others

**Modifying the ownership permissions:**

we use the chown command 
sudo chown username filename

simialrly, sudo chgrp Group_name filename

--If you use a colon : we can both username and group at the sametime
sudo chown username:Group_name filename

**umask:**

This umask command takes away the permissions of the file that are newly created
what I mean is there are default permissions given when a file is created. we can change that, this command takes the numerical input

umask 021

the above command takes nothing from users(0), takes away the write permission(2) and executable permission(1) from others

**SUID:**
There are times where users need elevated access to do stuff. The system administrator cannot always be there to enter the root password every time 
a user needs access to a protected file.
so there are special file permission bits that allow this behaviour. The set userID (SUID) allows a user to run a program as the owner of the program file rather 
than themselves.
when we type the command  ls -l /usr/bin/passwd, we will get something like -rwsr-xr-x 1 root root
Here s is the SUID, which enables you to run a program as the admin

**MOdifying suid**

symblic way:
sudo chmod u+s filename

Numerical way:
sudo chmod 4755 filename

As you can see the suid id denoted by 4 and prepended to the permission set

**GUID**
similarly to the set userID permission bit there is set GroupID bit SGID that allows a program to run as if it was a member of a group.

**Modifying SGID:**
sudo chmod g+s filename
sudo chmod 2555 filename
Here 2 represents GUID bit 

**The sticky Bit**
By adding this bit we can make a file/directory only root user can delete the file
't' is the sticky bit 

****Modify sticky bit ****
sudo chmod +t dirName
sudo chmod 1755 dirName

here 1 adds the sticky bit





