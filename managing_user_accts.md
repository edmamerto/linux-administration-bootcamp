# Managing Users

1.  Log into your Linux Essentials lab server and become the root user.

> ```
> su -
> ```

2.  We are going to create a new user. The user's full name is Mary Phillips. The username should be _mphillips_. The default shell should be the bourne again shell. After creating the user then set the password to _LinuxPassword_.

> useradd -c "Mary Phillips" -m  -s "/bin/bash" mphillips
> Note that while Ubuntu will create your home directory for you, some Linux distros do not do this for you. The `-m` flag is the option to have it created for you.
> passwd mphillips

3.  There is a specific file on the Linux file system in which we can verify that our new username was created; how would we view this?

> ```
> cat /etc/passwd
> ```

4.  Create a user account called _richard_, using all defaults.

> ```
> useradd richard
> ```

5.  Give the new user account, _richard_, a password of _LinuxPassword_ and a full name of _Richard Layton_.

> passwd richard
> usermod -c "Richard Layton" richard
