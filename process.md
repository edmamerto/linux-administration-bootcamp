# Process

> set of instructions loaded into a memory

PID 1 
> Process ID **1** is usually the init process primarily responsible for starting and shutting down the system.
> PID 1 is the parent process and all other processes are children

Init 
> In Linux, **init** is a abbreviation for Initialization. The **init** is a daemon process which starts as soon as the computer starts and continue running till, it is shutdown. In-fact init is the first process that starts when a computer boots, making it the parent of all other running processes directly or indirectly and hence typically it is assigned “**pid=1**“.

Systemd
> A  **systemd**  is a System Management Daemon named with UNIX convention to add ‘**d**‘ at the end of daemon. So, that they can be easily recognized. Initially it was released under GNU General Public License, but now the releases are made under GNU Lesser General Public License. Similar to init, systemd is the parent of all other processes directly or indirectly and is the first process that starts at boot hence typically assigned a “**pid=1**“.

> A  **systemd**, may refer to all the packages, utilities and libraries around daemon. It was designed to overcome the shortcomings of init. It itself is a background processes which is designed to start processes in parallel, thus reducing the boot time and computational overhead. It has a lot other features as compared to init.

/Proc
> Direct line of communication to the linux kernel
