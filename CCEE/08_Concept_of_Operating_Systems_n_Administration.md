> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 08

## **Session 7 : Linux OS**

---

### 1. A system administrator needs to create a new local user while ensuring compatibility across most Linux distributions and scripting environments. Which command is most appropriate?

* [ ] newuser
* [ ] adduser
* [ ] useradd
* [ ] createuser

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** useradd
💡 `useradd` is the low-level, standard Linux utility available on all distributions and preferred for automation and exam scenarios.

</details>

---

### 2. During a security audit, you are asked to identify the file that maintains basic user account metadata such as UID, GID, and shell. Which file fulfills this role?

* [ ] /etc/group
* [ ] /etc/passwd
* [ ] /home/user
* [ ] /etc/login

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/passwd
💡 `/etc/passwd` stores user account information excluding passwords, which are kept in `/etc/shadow`.

</details>

---

### 3. An administrator needs to temporarily switch to another user account for troubleshooting without logging out. Which command is designed for this purpose?

* [ ] chuser
* [ ] sudo
* [ ] login
* [ ] su

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** su
💡 `su` allows switching to another user’s shell, commonly used for privilege escalation or role switching.

</details>

---

### 4. When a new user is created using default settings on a modern Linux system, which group is typically assigned as the user’s primary group?

* [ ] admin
* [ ] wheel
* [ ] users
* [ ] Same as the username

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Same as the username
💡 Most Linux distributions use **User Private Groups (UPG)**, where a group with the same name as the user is created.

</details>

---

### 5. You want to quickly verify the effective identity of the current shell session, especially after privilege escalation. Which command provides this information?

* [ ] whoami
* [ ] id
* [ ] who
* [ ] echo user

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** whoami
💡 `whoami` displays the effective user running the current session.

</details>

---

### 6. A user reports that they cannot log in after a password change policy update. Which command is directly responsible for setting or modifying a user’s password?

* [ ] Resets the group
* [ ] Changes the user shell
* [ ] Changes the password
* [ ] Deletes the user

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Changes the password
💡 The `passwd` command updates authentication credentials stored securely in `/etc/shadow`.

</details>

---

### 7. During access review, you need to identify all supplementary groups a user belongs to. Which command gives this information?

* [ ] listgroup
* [ ] groups
* [ ] getgroup
* [ ] userlist

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** groups
💡 The `groups` command lists all group memberships for a user.

</details>

---

### 8. For security reasons, Linux separates authentication secrets from public user data. Which file securely stores hashed user passwords?

* [ ] /etc/passwd
* [ ] /etc/login.defs
* [ ] /etc/shadow
* [ ] /etc/security

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/shadow
💡 `/etc/shadow` is readable only by root and contains encrypted password hashes.

</details>

---

### 9. A system administrator wants to define a new access control group for developers. Which command is standard and portable across Linux systems?

* [ ] groupadd
* [ ] addgroup
* [ ] mkgroup
* [ ] creategroup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** groupadd
💡 `groupadd` is the core utility used to create new groups in Linux.

</details>

---

### 10. While creating a user, you want to explicitly specify a custom home directory path. Which `useradd` option is required?

* [ ] -m
* [ ] -h
* [ ] -d
* [ ] -p

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -d
💡 `-d` specifies the home directory location; `-m` only creates it.

</details>

---

### 11. To mitigate a suspected compromise, an administrator wants to immediately prevent user login without deleting the account. What is the correct approach?

* [ ] passwd -d
* [ ] passwd -l
* [ ] userdel -l
* [ ] usermod -x

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** passwd -l
💡 Locking the password disables authentication while preserving user data.

</details>

---

### 12. An organization needs to change a user’s shell and group memberships. Which command is designed for modifying existing users?

* [ ] modifyuser
* [ ] usermod
* [ ] changelogin
* [ ] useredit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** usermod
💡 `usermod` alters user properties such as shell, groups, UID, and expiry.

</details>

---

### 13. Which file defines group names, GIDs, and their member users?

* [ ] Encrypted passwords
* [ ] Group membership and definitions
* [ ] User profiles
* [ ] Shell configurations

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Group membership and definitions
💡 `/etc/group` centrally manages group information.

</details>

---

### 14. In Linux access control, what does the term *primary group* refer to?

* [ ] The main group assigned to a user
* [ ] A group with administrative rights
* [ ] The first group in /etc/group
* [ ] The root group

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The main group assigned to a user
💡 Files created by a user are assigned this group by default.

</details>

---

### 15. You want to add an existing user to a supplementary group without removing current memberships. Which command is correct?

* [ ] groupadd
* [ ] usermod -aG
* [ ] useradd -g
* [ ] chgroup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** usermod -aG
💡 `-aG` appends groups safely; omitting `-a` overwrites memberships.

</details>

---

### 16. While auditing permissions, which command shows both UID and GID of a user?

* [ ] whoami
* [ ] id
* [ ] users
* [ ] env

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** id
💡 `id` displays numeric and named identifiers for users and groups.

</details>

---

### 17. Which statement best describes the effect of executing `userdel username`?

* [ ] Deactivates a user temporarily
* [ ] Deletes a user
* [ ] Renames a user
* [ ] Removes a group

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deletes a user
💡 `userdel` removes the account but does not delete the home directory unless `-r` is used.

</details>

---

### 18. To change default settings applied during user creation (e.g., shell, expiry), which file is commonly modified?

* [ ] /etc/default/useradd
* [ ] /etc/userdefaults
* [ ] /etc/login.defs
* [ ] /etc/profile

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/default/useradd
💡 This file controls defaults used by the `useradd` command.

</details>

---

### 19. Which method reliably lists **all local users**, including system accounts?

* [ ] ls /home
* [ ] cat /etc/passwd
* [ ] who -u
* [ ] users

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** cat /etc/passwd
💡 `/etc/passwd` enumerates every user account on the system.

</details>

---

### 20. The `chage` command is primarily used for which security control?

* [ ] Change group
* [ ] Change user’s shell
* [ ] Set password expiration policy
* [ ] Change account permissions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Set password expiration policy
💡 `chage` enforces password aging, expiry, and inactivity rules.

</details>

---

### 21. In Linux privilege management, what does UID 0 signify?

* [ ] Guest user
* [ ] Any regular user
* [ ] Superuser (root)
* [ ] System daemon

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Superuser (root)
💡 UID 0 bypasses discretionary access controls.

</details>

---

### 22. In the `/etc/passwd` file structure, which field specifies the user’s default login shell?

* [ ] 5th field
* [ ] 6th field
* [ ] 7th field
* [ ] 8th field

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 7th field
💡 Field order: username, password placeholder, UID, GID, comment, home, shell.

</details>

---

### 23. A compliance policy mandates password change on next login. Which command enforces this immediately?

* [ ] passwd --expire username
* [ ] passwd -d username
* [ ] usermod -x username
* [ ] loginctl reset username

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** passwd --expire username
💡 Expiring the password forces reset upon next authentication.

</details>

---

### 24. Which description best defines a *system user* in Linux?

* [ ] User created with UID below 1000
* [ ] User with admin rights
* [ ] Guest account
* [ ] User created by other users

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** User created with UID below 1000
💡 System users run services and do not represent human logins.

</details>

---

### 25. To fully remove a user and all associated files from the system, which command is appropriate?

* [ ] userdel -r
* [ ] deluser -f
* [ ] rmuser --remove-home
* [ ] delhome user

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** userdel -r
💡 `-r` ensures home directory and mail spool removal.

</details>

---

### 26. An organization wants to enforce strong password complexity rules. Which configuration file is primarily used?

* [ ] /etc/shadow
* [ ] /etc/login.defs
* [ ] /etc/security/pwquality.conf
* [ ] /etc/default/useradd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/security/pwquality.conf
💡 This file works with PAM to enforce password strength policies.

</details>

---

### 27. Which command creates a user account **without** generating a home directory?

* [ ] useradd -d
* [ ] useradd -M
* [ ] useradd -H
* [ ] useradd --no-home

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** useradd -M
💡 `-M` suppresses home directory creation even if defaults exist.

</details>

---

### 28. Which PAM module is responsible for authenticating users against local UNIX credentials?

* [ ] pam_env.so
* [ ] pam_unix.so
* [ ] pam_tty.so
* [ ] pam_exec.so

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** pam_unix.so
💡 `pam_unix.so` handles standard password authentication.

</details>

---

### 29. How can an administrator review password aging and expiry information for a specific user?

* [ ] passwd -l username
* [ ] chage -l username
* [ ] usermod -E username
* [ ] expire -s username

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chage -l username
💡 Displays last change, expiry, inactivity, and warning periods.

</details>

---

### 30. Which log file is most commonly used to monitor authentication attempts on Debian-based systems?

* [ ] /var/log/login.log
* [ ] /var/log/user.log
* [ ] /var/log/auth.log
* [ ] /etc/secure.log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /var/log/auth.log
💡 Authentication, sudo, and PAM events are recorded here.

---

## **Session 7 : Linux OS**

---

### 1. A system administrator wants a summarized view of disk space consumed by directories to identify storage hogs. Which Linux command best serves this requirement?

* [ ] df
* [ ] lsblk
* [ ] du
* [ ] mount

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** du
💡 `du` (disk usage) reports disk space used by files and directories, making it ideal for identifying which directories consume the most storage.

</details>

---

### 2. While troubleshooting low disk space alerts, an analyst needs to view free and used space across all mounted filesystems. Which command should be used?

* [ ] free
* [ ] ls
* [ ] df
* [ ] blkid

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** df
💡 `df` displays filesystem-level disk space usage, including total, used, and available space for mounted filesystems.

</details>

---

### 3. During a forensic examination, you need a hierarchical view of all block devices, their partitions, and mount points. Which command provides this information?

* [ ] lspci
* [ ] lsblk
* [ ] mount
* [ ] blkid

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** lsblk
💡 `lsblk` shows block devices in a tree format, including disks, partitions, and mount points, aiding system analysis.

</details>

---

### 4. By default, the output of the `df` command displays disk usage in which unit?

* [ ] Bytes
* [ ] Kilobytes
* [ ] Megabytes
* [ ] Gigabytes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kilobytes
💡 `df` reports sizes in 1K blocks by default unless overridden using options like `-h` or `-B`.

</details>

---

### 5. Which command would you use to analyze disk usage of a specific directory and its subdirectories?

* [ ] du
* [ ] df
* [ ] pwd
* [ ] mount

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** du
💡 `du` recursively calculates disk usage for directories and files, unlike `df`, which operates at filesystem level.

</details>

---

### 6. What is the primary function of the `mount` command in Linux?

* [ ] Formats storage devices
* [ ] Attaches a filesystem to the directory tree
* [ ] Lists connected disks
* [ ] Compresses filesystems

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Attaches a filesystem to the directory tree
💡 `mount` makes a filesystem accessible by attaching it to a mount point within the Linux directory hierarchy.

</details>

---

### 7. Which configuration file defines filesystems that should be automatically mounted during system boot?

* [ ] /etc/mount.conf
* [ ] /etc/fstab
* [ ] /etc/init.d/mounts
* [ ] /proc/mounts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/fstab
💡 `/etc/fstab` contains static filesystem information used during boot to mount filesystems automatically.

</details>

---

### 8. An administrator must safely detach a filesystem before disk maintenance. Which command should be used?

* [ ] fsck
* [ ] umount
* [ ] eject
* [ ] swapoff

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** umount
💡 `umount` detaches a mounted filesystem, ensuring no active processes are accessing it.

</details>

---

### 9. Which command-line utility is traditionally used to create or modify disk partitions?

* [ ] mkfs
* [ ] lsblk
* [ ] fdisk
* [ ] mount

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** fdisk
💡 `fdisk` is a classic CLI partition editor used for MBR/GPT partition tables.

</details>

---

### 10. What is the primary role of the `mkfs` command?

* [ ] Mounting filesystems
* [ ] Creating a filesystem structure
* [ ] Verifying disk integrity
* [ ] Resizing partitions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Creating a filesystem structure
💡 `mkfs` initializes a filesystem on a partition after partitioning is completed.

</details>

---

### 11. Which command explicitly creates an ext4 filesystem on a partition?

* [ ] mkfs
* [ ] mkfs.ext4
* [ ] format.ext4
* [ ] ext4mk

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** mkfs.ext4
💡 `mkfs.ext4` ensures the filesystem type is ext4 without ambiguity.

</details>

---

### 12. Before mounting a potentially corrupted filesystem, which utility should be used to check and repair it?

* [ ] tune2fs
* [ ] fsck
* [ ] mount
* [ ] debugfs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** fsck
💡 `fsck` checks filesystem consistency and repairs errors to prevent data corruption.

</details>

---

### 13. On most Linux distributions, removable media such as USB drives are auto-mounted under which directory?

* [ ] /mnt
* [ ] /media
* [ ] /opt
* [ ] /run

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /media
💡 `/media` is commonly used by udev and desktop environments for removable media mount points.

</details>

---

### 14. In Linux device naming, what does `/dev/sda1` usually represent?

* [ ] First USB device
* [ ] First partition on the first SATA/SCSI disk
* [ ] RAM disk
* [ ] Network interface

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** First partition on the first SATA/SCSI disk
💡 `sda` denotes the first disk; `1` indicates its first partition.

</details>

---

### 15. Which command initializes a partition to be used as swap space?

* [ ] swapon
* [ ] mkfs.swap
* [ ] mkswap
* [ ] swapctl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** mkswap
💡 `mkswap` prepares a block device or partition for use as swap space.

</details>

---

### 16. After creating swap space, which command activates it?

* [ ] swapstart
* [ ] swapon
* [ ] mount -s
* [ ] enableswap

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** swapon
💡 `swapon` enables swap space for use by the kernel.

</details>

---

### 17. Which utility provides a graphical interface for disk partitioning?

* [ ] parted
* [ ] fdisk
* [ ] gparted
* [ ] mkpart

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** gparted
💡 `gparted` is a GUI frontend for partition management, commonly used on desktop Linux.

</details>

---

### 18. What type of information does `lsblk` primarily display?

* [ ] Network interfaces
* [ ] USB vendor details
* [ ] Block device topology
* [ ] Kernel boot messages

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Block device topology
💡 `lsblk` shows block devices, their relationships, mount points, and sizes.

</details>

---

### 19. What is the maximum supported file size on an ext3 filesystem (with 4KB block size)?

* [ ] 2GB
* [ ] 16GB
* [ ] 2TB
* [ ] 16TB

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 2TB
💡 ext3 supports files up to 2TB depending on block size and architecture.

</details>

---

### 20. Which command displays the UUIDs of block devices and filesystems?

* [ ] blkid
* [ ] lsblk -u
* [ ] uuidscan
* [ ] mount -u

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** blkid
💡 `blkid` retrieves filesystem UUIDs, commonly used in `/etc/fstab`.

</details>

---

### 21. What is the practical effect of mounting a filesystem as read-only?

* [ ] Files can be modified but not deleted
* [ ] Files can be read but not written
* [ ] Filesystem becomes inaccessible
* [ ] Filesystem auto-unmounts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Files can be read but not written
💡 Read-only mounts protect data integrity during recovery or forensic analysis.

</details>

---

### 22. Which tool is specifically used to resize an ext4 filesystem after partition resizing?

* [ ] fdisk
* [ ] growpart
* [ ] resize2fs
* [ ] tune2fs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** resize2fs
💡 `resize2fs` adjusts the size of ext2/ext3/ext4 filesystems.

</details>

---

### 23. What is a key advantage of Logical Volume Management (LVM)?

* [ ] Automatic disk encryption
* [ ] Flexible resizing of logical volumes
* [ ] Hardware RAID creation
* [ ] Filesystem journaling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Flexible resizing of logical volumes
💡 LVM allows dynamic resizing and management of storage without downtime.

</details>

---

### 24. During boot troubleshooting, which log file commonly records filesystem mount errors?

* [ ] /etc/fstab
* [ ] /var/log/dmesg
* [ ] /var/log/syslog
* [ ] /var/log/mount.log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /var/log/syslog
💡 `syslog` captures system-wide events, including mount failures during boot.

</details>

---

### 25. What is the most common logical sector size used by modern disks?

* [ ] 256 bytes
* [ ] 512 bytes
* [ ] 1024 bytes
* [ ] 4096 bytes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 512 bytes
💡 While 4K sectors exist, most disks expose 512-byte logical sectors for compatibility.

</details>

---

### 26. What information is provided by `/proc/partitions`?

* [ ] Mounted filesystems
* [ ] Filesystem configuration
* [ ] Kernel-recognized partition details
* [ ] Disk cache statistics

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kernel-recognized partition details
💡 `/proc/partitions` shows block devices and partitions known to the kernel.

</details>

---

### 27. What is the primary function of the `tune2fs` utility?

* [ ] Kernel tuning
* [ ] Filesystem parameter modification
* [ ] Disk repartitioning
* [ ] RAID configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Filesystem parameter modification
💡 `tune2fs` adjusts ext filesystem parameters such as reserved blocks and mount counts.

</details>

---

### 28. What is the effect of using the `noatime` mount option?

* [ ] Disables filesystem logging
* [ ] Prevents access time updates
* [ ] Forces synchronous writes
* [ ] Hides filesystem metadata

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevents access time updates
💡 `noatime` improves performance by disabling updates to file access timestamps.

</details>

---

### 29. Which command is used to edit user or group disk quotas?

* [ ] fsquota
* [ ] edquota
* [ ] quotaedit
* [ ] disklimit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** edquota
💡 `edquota` edits quota limits assigned to users or groups.

</details>

---

### 30. What is the effect of executing `mount -o loop file.iso /mnt`?

* [ ] Formats the ISO file
* [ ] Mounts the ISO as a loopback filesystem
* [ ] Extracts ISO contents
* [ ] Converts ISO to block device

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mounts the ISO as a loopback filesystem
💡 Loop mounting allows disk images to be accessed like physical filesystems.

</details>

---
