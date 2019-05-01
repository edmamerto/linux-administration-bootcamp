### Dev Null
https://medium.com/@codenameyau/step-by-step-breakdown-of-dev-null-a0f516f53158

> To begin, /dev/null is a special file called the null device in Unix systems. Colloquially it is also called the bit-bucket or the blackhole because it immediately discards anything written to it and only returns an end-of-file EOF when read.

write something to it
```
$ echo 'text' > /dev/null
```
check if write was successful
```
$ echo $?
0
```
>The `$?` symbol is a special variable that always contains the exit status of the previous command;
Now let’s look at the invalid command:
```
$ ls -0
ls: illegal option -- 0
usage: ls [-ABCFGHLOPRSTUWabcdefghiklmnopqrstuwx1] [file ...]
```
check status
```
$ echo $?
1
```
The problem with the second script is that it displays any error messages into `STDERR`. However for our scripts, we want to suppress error messages. Luckily there’s a hack to do exactly what we want.

Let’s try that again with > /dev/null 2>&1:
```
$ ls -0 > /dev/null 2>&1
$ echo $?
1
```

Notice this time, that we didn’t see any error messages. To break this down, we’re suppressing the error output (stderr) of the ls -0 command, redirect it to standard output (stdout), writing it to /dev/null thereby immediately discarding it. The >& symbol is an operator that copies the output of the first file descriptor (2) and redirects to the output of the second file descriptor (1).

Now let’s see what the numbers in `2>&1` represent by looking at this chart of File Descriptors.

We can verify this by outputting to a regular file instead of `/dev/null`.
```
$ ls -0 > /tmp/devnull 2>&1
```
```
$ echo $?
1
```
```
$ cat /tmp/devnull
ls: illegal option -- 0
usage: ls [-ABCFGHLOPRSTUWabcdefghiklmnopqrstuwx1] [file ...]
```

```
+--------+---+
| stdin  | 0 |
+--------+---+
| stdout | 1 |
+--------+---+
| stderr | 2 |
+--------+---+
```
This technique is commonly used to tell whether a command exists, which you can use for handling different operating systems, automatically installing packages, downloading files, and most importantly defending your scripts and systems from unexpected exceptions.
```
function cmd_exists() {
  command -v $1 > /dev/null 2>&1
}
# cmd_exists ls; echo $?
# cmd_exists sl; echo $?
```
