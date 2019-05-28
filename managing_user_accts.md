Log into your Linux Essentials lab server and become the root user.
su -
We are going to create a new user.  The user's full name is Mary Phillips. The username should be mphillips.  The default shell should be the bourne again shell.  After creating the user then set the password to LinuxPassword.
useradd -c "Mary Phillips" -m  -s "/bin/bash" mphillips
Note that while Ubuntu will create your home directory for you, some Linux distros do not do this for you. The -m flag is the option to have it created for you.
passwd mphillips
There is a specific file on the Linux file system in which we can verify that our new username was created; how would we view this?
cat /etc/passwd
Create a user account called richard, using all defaults.
useradd richard
Give the new user account, richard, a password of LinuxPassword and a full name of Richard Layton.
passwd richard
usermod -c "Richard Layton" richard
