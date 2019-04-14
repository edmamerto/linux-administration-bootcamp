### Directories
> Leaning Directories

- It is a storage location that has a name and a value
- Typically uppercase

Access the contents by executing
```
$ echo $VAR_NAME
```
$PATH
> - Controls the command search path
> - Contains a list of directories that are separated by colon
> - Tells your computer where to look for executable programs

$PATH == "Controls the command search path"
> What we mean by when you type in the command at the prompt and press enter, that command will be searched for in the directories

In this example, /usr/local/bin will be searched first.
```
echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

Find path of command
```
$ which cat
```
### Directories

Period .
> When working on Linux systems, a period is often referred to as 'dir'.

Creating directory structure that is more than one directory deep
```
mkdir -p 1/2/3
```
Remove empty directories
```
rmdir
```
*When you delete something, it's gone. No undo.*

Listing Files by Type
```
$ ls -F
```
```
/ Directory
@ Link 
* Executable
```
Symbolic Links
> Looks like a file or directory, but it just points to where the actual file or directory is 

Tree
```
tree -d # List directories only
ytrr -C # Colorize output
```