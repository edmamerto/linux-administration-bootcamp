### Permissions
> Learning Permissions

```
$ ls -l
-rw-rw-r-- 1 ed users 10400 Aug 6 08:52 hell.data
```
```
+--------+---------------+
| Symbol | Type          |   
+--------+---------------+
| -      | Regular file  |
+--------+---------------+
| d      | Directory     |
+--------+---------------+
| l      | Symbolic Link |
+--------+---------------+
```
Changing Permissions
```
+-------+----------------------------------------+
| Item  | Meaning                                |
+-------+----------------------------------------+
| chmod | Change mode command                    |
+-------+----------------------------------------+
| ugoa  | User category: user, group, other, all |
+-------+----------------------------------------+
| +-=   | Symbolic Link                          |
+-------+----------------------------------------+
```
Example: give write perms to group
```
$ chmod g+w hello.data
```
Remove write perms to group
```
$ chmod g-w hello.data
```