### Find
> cheatsheet

*link*

 - https://www.youtube.com/watch?v=KCVaNb_zOuw

Return all files and dirs in the the current directory
```
$ find .
```
find only dirs and exclude files
```
$ find -type d
```
find only files exlude dirs
```
$ find -type f
```
find specific file
```
$ find . -type f -name "test.xt"
```
find files that start with test (case sensitive)
```
$ find . -type f -name "test*" 
```
find files that start with test (case insensitive)
```
$ find . -type f -iname "test*" 
```
find all python files
```
$ find . -type f -iname "*.py" 
```
find files modified in the last 10 minutes
```
$ find -type f -mmin -10
```
find files modified more than 10 minutea ago
```
$ find -type f -mmin +10
```
find files modified more than 1 minute ago and less than 5 minutes ago
```
$ find -type f -mmin +1 -mmin -5
```
find files over 5megabytes
```
$ find . -size +5M 
```
find empty files
```
$ find . -empty
```
find files of a specific permission
```
$ find -perm 777
```
find files and change owner and group
```
$ find . -exec chown edmamerto:mygroup {} +
```
>`{}` placeholder
`+` end command (terminator)





