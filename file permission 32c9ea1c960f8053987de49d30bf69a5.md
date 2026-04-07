# file permission

ls -a

ls -la

read= 4 write= 2 execute= 1

## change file permission:

- chmod 000 filename
- chmod 777 filename
- chmod 640 filename

## change ownership:

- chown <usernname> <filename>
- chown <usernname>:<groupname> <filename>

## change group:

- chgrp <groupname> <filename>

## change shell:

- chsh -s /usr/bin/bash <username>
- echo $SHELL
- which bash

switch user:

- su -c ‘command’ <username>

`setfacl` is a Linux command used to set **Access Control Lists (ACLs)**
It lets you give specific users or groups access to files **without changing ownership**.

`example: setfacl -m u:john:rw file.txt`

`setfacl -m g:devs:rwx project/`

`syntax: setfacl [options] <permissions> <file>`

check ACLs: `getfacl file.txt`