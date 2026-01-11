> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 02


## **Session 1: Linux Essentials**

### 1. Which of the following is a Linux distribution commonly used in servers and desktops?

* [ ] Windows XP
* [ ] macOS
* [ ] Ubuntu
* [ ] DOS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ubuntu
💡 Ubuntu is a widely used Linux distribution suitable for desktops and servers. Windows XP, macOS, and DOS are non-Linux operating systems.

</details>

---

### 2. In Linux, what does the tilde symbol (~) represent in commands?

* [ ] Shell prompt
* [ ] Home directory of the current user
* [ ] Root directory
* [ ] Hidden files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Home directory of the current user
💡 The tilde (~) expands to the current user's home directory path, e.g., /home/username.

</details>

---

### 3. You want to see a detailed listing of files including permissions and sizes. Which command should you use?

* [ ] list
* [ ] dir
* [ ] ls -l
* [ ] show

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ls -l
💡 The `ls -l` command lists files in long format, displaying permissions, owner, group, size, and modification date.

</details>

---

### 4. Which of the following best describes the root user in Linux?

* [ ] Limited access
* [ ] No access
* [ ] Administrative access
* [ ] Read-only access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Administrative access
💡 The root user has unrestricted access to all files, commands, and system resources.

</details>

---

### 5. While running a long process in the terminal, which key combination will safely terminate it?

* [ ] Ctrl + D
* [ ] Ctrl + C
* [ ] Ctrl + A
* [ ] Ctrl + Z

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ctrl + C
💡 Ctrl + C sends the SIGINT signal to terminate a running foreground process.

</details>

---

### 6. Which shell is the default in most modern Linux distributions?

* [ ] csh
* [ ] bash
* [ ] fish
* [ ] powershell

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** bash
💡 Bash (Bourne Again Shell) is the default interactive shell in most Linux distributions.

</details>

---

### 7. Which command displays the absolute path of your current working directory?

* [ ] pwd
* [ ] cd
* [ ] dir
* [ ] where

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** pwd
💡 `pwd` (print working directory) outputs the full path of the current directory.

</details>

---

### 8. You need to change a file’s permissions. Which command is appropriate?

* [ ] chmod
* [ ] chperm
* [ ] chown
* [ ] perm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chmod
💡 `chmod` is used to set read, write, and execute permissions for files or directories.

</details>

---

### 9. To navigate to the parent directory of your current location, you should use:

* [ ] cd ..
* [ ] cd /
* [ ] cd ~
* [ ] cd .

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** cd ..
💡 `cd ..` moves the user up one level in the directory hierarchy.

</details>

---

### 10. Which command allows you to view only the first few lines of a file for quick inspection?

* [ ] top
* [ ] head
* [ ] tail
* [ ] less

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** head
💡 `head filename` displays the first 10 lines of a file by default.

</details>

---

### 11. What information does `ls -l` provide?

* [ ] Only large files
* [ ] Long listing format including permissions, owner, and size
* [ ] Locked files
* [ ] Files in lowercase

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Long listing format including permissions, owner, and size
💡 `ls -l` shows file details such as permissions, number of links, owner, group, size, and modification date.

</details>

---

### 12. You want to rename a file or move it to another directory. Which command should you use?

* [ ] rm
* [ ] mv
* [ ] cp
* [ ] rename

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** mv
💡 The `mv` command is used to move files/directories or rename them.

</details>

---

### 13. Which command duplicates files or directories in Linux?

* [ ] mv
* [ ] copy
* [ ] cp
* [ ] du

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** cp
💡 `cp` copies files or directories. `mv` moves files.

</details>

---

### 14. How do you create a new, empty file in Linux without opening an editor?

* [ ] make file.txt
* [ ] touch file.txt
* [ ] new file.txt
* [ ] mk file.txt

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** touch file.txt
💡 The `touch` command updates timestamps or creates an empty file if it does not exist.

</details>

---

### 15. Which command displays the contents of a file on the terminal?

* [ ] show
* [ ] list
* [ ] cat
* [ ] read

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** cat
💡 `cat filename` outputs the full content of the file to the standard output.

</details>

---

### 16. Which command provides detailed documentation about other Linux commands?

* [ ] Opens file manager
* [ ] Displays system info
* [ ] Displays manual pages
* [ ] Installs packages

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Displays manual pages
💡 `man command` displays the manual for any Linux command, including options and usage.

</details>

---

### 17. What does `rm -r` do when applied to a directory?

* [ ] Removes regular files only
* [ ] Removes read-only files
* [ ] Removes directories and all their contents recursively
* [ ] Renames directories

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Removes directories and all their contents recursively
💡 `rm -r directory` deletes the directory along with all nested files and directories.

</details>

---

### 18. Which command reveals the path of an executable command?

* [ ] where
* [ ] find
* [ ] locate
* [ ] which

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** which
💡 `which command` shows the full path of the executable that would run for that command.

</details>

---

### 19. To display hidden files in a directory using `ls`, which option is used?

* [ ] -l
* [ ] -a
* [ ] -r
* [ ] -h

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -a
💡 `ls -a` lists all files, including hidden files starting with `.`.

</details>

---

### 20. Which command changes the owner of a file?

* [ ] chmod
* [ ] ownfile
* [ ] chown
* [ ] chperm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chown
💡 `chown newowner filename` changes the ownership of a file or directory.

</details>

---

### 21. Where are Linux system configuration files typically stored?

* [ ] /bin
* [ ] /etc
* [ ] /usr
* [ ] /dev

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc
💡 `/etc` contains configuration files for the system and installed services.

</details>

---

### 22. What does `find / -type f -name "*.log"` accomplish?

* [ ] Finds log files in the current directory
* [ ] Finds all directories ending with .log
* [ ] Finds all files with .log extension starting from root
* [ ] Lists recent logs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Finds all files with .log extension starting from root
💡 `find` recursively searches starting from `/` for regular files (`-type f`) with names matching `*.log`.

</details>

---

### 23. Which file contains user account information in Linux?

* [ ] /etc/shadow
* [ ] /etc/passwd
* [ ] /etc/user
* [ ] /etc/accounts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/passwd
💡 `/etc/passwd` contains basic account info; `/etc/shadow` stores hashed passwords.

</details>

---

### 24. How can you change both the owner and group of a file simultaneously?

* [ ] chgrp
* [ ] chmod
* [ ] chown user:group file
* [ ] own

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chown user:group file
💡 Syntax `chown user:group filename` modifies both owner and group in one command.

</details>

---

### 25. Which statement correctly differentiates a hard link from a soft link in Linux?

* [ ] Hard link points to a different file
* [ ] Soft link duplicates the file
* [ ] Soft link points to the file path, hard link points to inode
* [ ] Both are the same

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Soft link points to the file path, hard link points to inode
💡 Hard links share the same inode; soft links (symlinks) reference the file path.

</details>

---

### 26. Which permission set corresponds to numeric mode 755?

* [ ] rwxrw-r--
* [ ] rwxr-xr-x
* [ ] rw-r--r--
* [ ] r-xr-xr-x

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** rwxr-xr-x
💡 7=owner rwx, 5=group r-x, 5=others r-x.

</details>

---

### 27. What does `du -sh /home/user` display?

* [ ] Shows disk usage of system
* [ ] Summarizes size of home directory in human-readable format
* [ ] Deletes files in home
* [ ] Shows system health

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Summarizes size of home directory in human-readable format
💡 `du -sh` summarizes total size of a directory, using units like K, M, or G.

</details>

---

### 28. Which description best fits the Linux file system structure?

* [ ] Hierarchical tree
* [ ] Flat file system
* [ ] Circular referencing
* [ ] Drive-letter based

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hierarchical tree
💡 Linux organizes files in a single root (`/`) with directories forming a hierarchical tree.

</details>

---

### 29. What is the primary purpose of `/var/log`?

* [ ] Holds temporary files
* [ ] Contains user files
* [ ] Stores system log files
* [ ] Backup directory

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Stores system log files
💡 `/var/log` contains system and application logs for auditing and troubleshooting.

</details>

---

### 30. What does `grep -i "error" logfile.txt` do?

* [ ] Searches for lowercase "error" only
* [ ] Ignores the file
* [ ] Searches "error" case-insensitively in logfile.txt
* [ ] Returns number of errors

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Searches "error" case-insensitively in logfile.txt
💡 The `-i` flag makes the search case-insensitive.

</details>

---

## **Session 2: Linux & Networking Advanced**

### 1. In Linux, what is the primary purpose of the `chmod` command?

* [ ] Changes the file owner
* [ ] Changes file permissions
* [ ] Moves a file
* [ ] Deletes a file

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Changes file permissions
💡 `chmod` modifies read, write, and execute permissions for files or directories.

</details>

---

### 2. Which command is used to change the ownership of a file in Linux?

* [ ] chmod
* [ ] chperm
* [ ] chown
* [ ] changeowner

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chown
💡 `chown user file` assigns a new owner to the specified file or directory.

</details>

---

### 3. Which protocol allows secure, encrypted access to a remote system?

* [ ] ftp
* [ ] ssh
* [ ] telnet
* [ ] ping

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ssh
💡 SSH encrypts communication, unlike telnet or FTP which are insecure.

</details>

---

### 4. Which of the following is considered secondary storage in a computer system?

* [ ] RAM
* [ ] CPU
* [ ] Hard Disk
* [ ] Cache

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hard Disk
💡 Secondary storage retains data permanently; RAM and cache are primary memory.

</details>

---

### 5. Which Linux command provides information about the current user?

* [ ] whoami
* [ ] finger
* [ ] id
* [ ] passwd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** whoami
💡 `whoami` prints the username of the currently logged-in user.

</details>

---

### 6. What does FTP stand for?

* [ ] File Transfer Protocol
* [ ] File Tunnel Port
* [ ] Fast Transfer Port
* [ ] File Traffic Program

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File Transfer Protocol
💡 FTP is a standard network protocol for transferring files between systems.

</details>

---

### 7. Which of the following is an optical storage medium?

* [ ] CD-ROM
* [ ] SSD
* [ ] RAM
* [ ] Hard Drive

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CD-ROM
💡 CD-ROMs use lasers to read/write data, classifying them as optical media.

</details>

---

### 8. What effect does `chmod 755 file.txt` have?

* [ ] Makes the file unreadable
* [ ] Grants full permissions to owner and read-execute to group and others
* [ ] Deletes the file
* [ ] Hides the file

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Grants full permissions to owner and read-execute to group and others
💡 7=rwx for owner, 5=r-x for group and others.

</details>

---

### 9. To recursively change ownership of a directory and its contents, which command is correct?

* [ ] chmod -R
* [ ] chown -R
* [ ] owner -r
* [ ] perm -r

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chown -R
💡 The `-R` option applies the ownership change to all nested files and directories.

</details>

---

### 10. What does the `umask` command influence?

* [ ] File visibility
* [ ] Default permissions for newly created files and directories
* [ ] File ownership
* [ ] Network configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Default permissions for newly created files and directories
💡 `umask` sets permission bits that are *masked out* when new files/directories are created.

</details>

---

### 11. Which protocol provides encrypted file transfers over a network?

* [ ] ftp
* [ ] telnet
* [ ] sftp
* [ ] http

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** sftp
💡 SFTP (Secure File Transfer Protocol) encrypts both commands and data over SSH.

</details>

---

### 12. Which command initiates a Telnet session to a host?

* [ ] connect [host]
* [ ] telnet [host]
* [ ] ssh [host]
* [ ] ftp [host]

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** telnet [host]
💡 `telnet` connects to a remote system over TCP, typically unencrypted.

</details>

---

### 13. `ls -l` displays file permissions. What does it show?

* [ ] Only read permissions
* [ ] Only write permissions
* [ ] Full permission string like rwxr-xr--
* [ ] No permission info

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Full permission string like rwxr-xr--
💡 The permission string includes read (r), write (w), execute (x) for owner, group, and others.

</details>

---

### 14. Where are mounted storage devices typically found in Linux?

* [ ] /media or /mnt
* [ ] /etc
* [ ] /boot
* [ ] /dev/null

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /media or /mnt
💡 These directories are standard mount points for external or temporary storage.

</details>

---

### 15. Which command formats a partition with the ext4 file system?

* [ ] mkfs.ext4
* [ ] fdisk -f
* [ ] format
* [ ] mkext4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** mkfs.ext4
💡 `mkfs.ext4 /dev/sdX` creates an ext4 filesystem on the specified partition.

</details>

---

### 16. Which command lists all connected storage devices?

* [ ] fdisk -l
* [ ] diskview
* [ ] devices
* [ ] hddinfo

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** fdisk -l
💡 `fdisk -l` displays all disk partitions and storage devices recognized by the system.

</details>

---

### 17. What is the purpose of `/etc/fstab`?

* [ ] To monitor running processes
* [ ] To log users
* [ ] To auto-mount storage devices at boot
* [ ] To list startup applications

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To auto-mount storage devices at boot
💡 `/etc/fstab` defines devices, mount points, and options for automatic mounting.

</details>

---

### 18. Which command allows secure copying of files between systems?

* [ ] scp
* [ ] copy
* [ ] sftp cp
* [ ] ftpcopy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** scp
💡 `scp` uses SSH to securely copy files between local and remote hosts.

</details>

---

### 19. What additional information does `ls -n` show compared to `ls -l`?

* [ ] File name
* [ ] File size
* [ ] Numeric user/group IDs
* [ ] Date of modification

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Numeric user/group IDs
💡 `ls -n` shows UID/GID instead of username/group name.

</details>

---

### 20. Which file system is commonly used for CD-ROMs in Linux?

* [ ] ext4
* [ ] ntfs
* [ ] iso9660
* [ ] btrfs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** iso9660
💡 ISO 9660 is the standard filesystem for optical media like CDs.

</details>

---

### 21. Which command shows current network connections and open ports?

* [ ] ps
* [ ] netstat
* [ ] ifconfig
* [ ] route

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** netstat
💡 `netstat -tuln` lists TCP/UDP ports and active network connections.

</details>

---

### 22. Which chmod setting grants read, write, execute only to the file owner?

* [ ] 777
* [ ] 644
* [ ] 700
* [ ] 755

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 700
💡 Owner has rwx; group and others have no permissions.

</details>

---

### 23. Which command displays Access Control List (ACL) entries of a file?

* [ ] aclshow
* [ ] getfacl
* [ ] showacl
* [ ] listacl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** getfacl
💡 `getfacl filename` lists ACL permissions beyond standard rwx bits.

</details>

---

### 24. How do you give user 'alex' read permission to `data.txt` using ACL?

* [ ] setfacl -m u:alex:r data.txt
* [ ] chmod u+rx alex data.txt
* [ ] chown alex data.txt
* [ ] getfacl -u alex data.txt

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** setfacl -m u:alex:r data.txt
💡 `setfacl` modifies ACLs to grant specific permissions to users or groups.

</details>

---

### 25. Which command mounts a USB device at `/mnt/usb`?

* [ ] attach usb /mnt/usb
* [ ] mount /dev/sdb1 /mnt/usb
* [ ] usbconnect /mnt/usb
* [ ] mount usb0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** mount /dev/sdb1 /mnt/usb
💡 `mount /dev/sdXN /mount/point` is the standard syntax for mounting devices.

</details>

---

### 26. Which command is used to create a new disk partition?

* [ ] mount
* [ ] fdisk
* [ ] mkfs
* [ ] chmod

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** fdisk
💡 `fdisk` is used for creating, deleting, and modifying disk partitions.

</details>

---

### 27. What effect does `chmod 2750 file` have?

* [ ] No effect
* [ ] Adds sticky bit
* [ ] Sets SGID with rwx for owner and rx for group
* [ ] Gives all users full access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Sets SGID with rwx for owner and rx for group
💡 `2` sets the SGID; 7=owner rwx, 5=group r-x, 0=others none.

</details>

---

### 28. Which Linux tool allows low-level formatting of a disk?

* [ ] dd
* [ ] mkfs
* [ ] parted
* [ ] fdisk

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dd
💡 `dd` can overwrite entire disks with zeros or patterns, useful for low-level formatting.

</details>

---

### 29. What is the purpose of the sticky bit on a directory?

* [ ] Allows all users to edit files
* [ ] Prevents deletion of files by non-owners
* [ ] Encrypts the files in directory
* [ ] Enables hidden mode

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevents deletion of files by non-owners
💡 Sticky bit is used on shared directories (e.g., `/tmp`) to restrict file deletion.

</details>

---

### 30. Which command can test port connectivity to a remote host?

* [ ] netstat
* [ ] ping
* [ ] telnet [host] [port]
* [ ] whois

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** telnet [host] [port]
💡 Telnet can attempt a TCP connection to a specific port to test connectivity.

</details>

---

### 31. Which command displays disk usage of files and directories in human-readable format?

* [ ] ls -lh
* [ ] df -h
* [ ] du -sh
* [ ] free -h

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** du -sh
💡 `du -sh` summarizes the disk usage of a directory in KB, MB, or GB.

</details>

---

### 32. Which command shows currently running processes with CPU and memory usage?

* [ ] top
* [ ] ps
* [ ] htop
* [ ] netstat

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** top
💡 `top` provides dynamic real-time display of running processes and resource usage.

</details>

---

### 33. Which Linux command can be used to check network interface configurations?

* [ ] ping
* [ ] ifconfig
* [ ] traceroute
* [ ] route

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ifconfig
💡 `ifconfig` shows IP addresses, netmask, and network interface status.

</details>

---

### 34. What is the primary function of the `tar` command?

* [ ] Transfer files over network
* [ ] Display disk usage
* [ ] Archive or extract files
* [ ] List running processes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Archive or extract files
💡 `tar` can combine multiple files into a single archive or extract them.

</details>

---

### 35. Which command checks the amount of free and used memory in Linux?

* [ ] df -h
* [ ] top
* [ ] free -h
* [ ] vmstat

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** free -h
💡 `free -h` displays RAM and swap usage in human-readable format.

</details>

---

### 36. Which option of `ls` lists files sorted by modification time?

* [ ] -a
* [ ] -lt
* [ ] -r
* [ ] -n

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -lt
💡 `ls -lt` sorts files in long format (`-l`) by modification time (`-t`).

</details>

---

### 37. Which command permanently deletes a file without moving it to trash?

* [ ] rm
* [ ] del
* [ ] shred
* [ ] erase

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** rm
💡 `rm filename` deletes a file immediately; `shred` overwrites it for secure deletion.

</details>

---

### 38. Which command shows the routing table of a Linux system?

* [ ] ifconfig
* [ ] ping
* [ ] route
* [ ] netstat

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** route
💡 `route -n` displays the IP routing table, including gateways and interface mappings.

</details>

---

### 39. Which command displays real-time log output from `/var/log/syslog`?

* [ ] tail -f /var/log/syslog
* [ ] cat /var/log/syslog
* [ ] less /var/log/syslog
* [ ] head /var/log/syslog

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** tail -f /var/log/syslog
💡 `tail -f` shows new log entries as they are appended.

</details>

---

### 40. Which command checks connectivity to a remote host by sending ICMP packets?

* [ ] ping
* [ ] traceroute
* [ ] netstat
* [ ] ssh

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ping
💡 `ping host` tests network reachability using ICMP echo requests.

</details>

---
