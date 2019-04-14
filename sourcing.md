### Source and Fork your Scripts
> This is a mini bootcamp

`source` From wikipedia
>source is a Unix command that evaluates the file following the command, as a list of commands, executed in the current context.[1] Frequently the "current context" is a terminal window into which the user is typing commands during an interactive session.
Process id of currently running process of your 
shell
```
echo $$
4321
```
*We can remember this number to know which shell something is running in* 

Create a simple shell script
```
$ sublime ~/scripts/ed_test.sh
```
```
#! /bin/bash
echo $$
```
```
$ chmod +x !$
```
Run the script
```
$ !e
$ ed_test.sh
1234
```
*they are not equal `1234 != 4321`, this means it ran in a separate bash process* 

Now let's try this 

Edit script
```
$ sublime ~/scripts/ed_test.sh
```
```
#! /bin/bash
username=ed
echo $username
```
Try
```
$echo
>
```
Then try
```
$ ed_test.sh
> ed
```
to get the variable in your current context you can `source` the file
```
$ source ed_test.sh
> ed
```
Typically we source `.bashrc` to reload environment variables

The following files are scripts that bash runs whenever. They're`initalization files`
```
/bin/bash
       The bash executable
/etc/profile
       The systemwide initialization file, executed for login shells
~/.bash_profile
       The personal initialization file, executed for login shells
~/.bashrc
       The individual per-interactive-shell startup file
~/.bash_logout
       The individual login shell cleanup file, executed when a login shell exits
```
