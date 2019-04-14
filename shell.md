### Shell
> Leaning Shell

Shell
> Default user interface to a Linux System
> A program that accepts your commands and executes those commands
> A command line interpreter

The Prompt
> When the shell is started it displays a prompt or shell prompt
```
[ed@linuxsvr]$
```
> username@hostname
> 
**$** is an indication that you're using the system as a normal user as opposed to a super user.

> The super user shell prompt ends typically with a pound sign 
```
[ed@linuxsvr]#
```
Root
> The super user is also called root

Root confusion
> When someone talks about root, they're either talking about slash - the beginning of the file system or the super user account named root

Normal vs Super user
> Normal user accounts can only do a subset of things that root can do

Typical Use Case for root access

- Install app outside of home dir
- stopt/start some apps i.e. webserver

Tilde in prompt
> represents a home directory

For example if I am logged in as `ed` 
```
~ == /home/ed
```