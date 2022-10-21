# Linux Security

## Access Controls

## PAM

pluggable authentication model

## Network Security

restrict/allow access services to network

## SSH Hardening

Secure shell - for remote access to network through unsecure network

## SELinux

security policies for insolating application running on the same system

## Others

## Linux Accounts

- UID, unique `/etc/passwd/

linux group - organize users into commen ations, each group contains GID
/etc/group

a user contains
username, uid GID (multiple ), if not exit then GID = UID, home directory, default shell
`id $idname` to get the gid.

Superuser - root, UID = 0, unlimited access

ssytem accounts - UID < 100 or 500-1000, ssh, mail etc. but dedicated home directory

service accounts (nginx, mercury)

`id` gives information about the user.
`who` all current logged in user
`last` all logged in user and the date and tiem system last reboot
`su` switch users, not reccomended use because requires passwrod.

`sudo` better way because own passwrod is required
`/etc/sudoers`kja defines the config. only users listed in the file can use sudo

## Managing users

need to run as root
`useradd` to add users
-c custom comments
-d custom home directory
-e expiry date
-g GID
-G multiple secondary groups
-s login shells
-u specific UID
`passwd username` to change the passwrod

`userdel` to delete users
`grooupadd` to add groups
`groupdel` to delete grops

## ACcess control Files

mostly in /etc
readable by most file
writable by root
not support by editors, but support commands

/etc/passwd
USERNAME:PASSWORD:UID:GID:GECOS:HOMEDIR:SHELL

/etc/shadow passwor
USERNAME:PASSWORD:LASTCHANGE:MINAGE:MAXAGE:WARN:INACTIVE:EXPDATE

/etc/group shows groups
NAME:PASSWORD:GID:MEMBERS

## File Permissions and ownsership

-_rwx_ rwx r-x
owner, group, others

r - read, octal value 4
w - write, octal value 2
x - execute octal value 1

- - no permission value 0

same applies to permissions

permissions are checked sequentially, of the owner try to access, then owner permission applies, otherwise group permissions apply

### Modify the file permission

`chmod permissions file`
`chmod u+rwx test-file` provide full access to owners
`chmod ugo+r-x test-file` provide read access to owners, grous and others. remove exeute access

modifyin permissions using numeric mode
`chmod 777 test-file` all access etc.
7, 6, 4, 3, 2 , 1,0

### Modifying ownership of the file

`chown owner:group filename`
`chgrp`

## SSH and SCP

### Password-less SSH

Key pair = private key + publi key

# ssh-keygen -t rsa

`ssh-copy-id username@server`

### SCP

copy files and directory between servers

## IPTABLES

`sudo apt install iptables` on ubunto OS
`sudo iptables -L` to list the rules

- `-A` add rule
- -p protocol
- -s source
- -d destination
- --dport destination port
- -j action to take

## CRON

`crontab -e` opens cron config file

minute | hour | day | month | weekday

stepvalue \*/2

`contab -l` to list all the jobs
/var/log/syslog logs the information of the cron jobs
