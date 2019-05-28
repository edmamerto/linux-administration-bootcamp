# Hardware

View the cpuinfo file to gather details on the processor
```
$ cat /proc/cpuinfo
```
View RAM statistics
```
$ free 
```
>-m = show output in MB
> -g = show output in GB

Show details about the motherboard, BIOS, processor and RAM on a system 
```
$ dmidecode 
```
View all block devices (such as hard disks) attached to the system
```
$ lsblk
```
View  free disk space on a hard disk
```
$ df -h
```
> -h show output in human readable format

show statistics on the processor, RAM, and running processes
```
$ top
```
In windows if hardrives are in `\C:` `\B:` whatever in Linux hardrives are in found in 
```
/dev/sda
/dev/sdb
/dev/sdc
```
> note that it in the dev folder and named `sd[a-z]`

