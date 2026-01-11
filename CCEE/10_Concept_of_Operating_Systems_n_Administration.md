> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 10

## **Session 10 : Linux OS**

---

### 1. In a systemd-based Linux distribution, an administrator wants to immediately start the Apache web server without enabling it at boot. Which command should be used?

* [ ] runservice apache2
* [ ] startsvc apache2
* [ ] systemctl start apache2
* [ ] services start apache2

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl start apache2
💡 `systemctl start` starts a service immediately under systemd without modifying its boot-time behavior.

</details>

---

### 2. The `systemctl` utility in Linux is primarily responsible for managing which of the following?

* [ ] Network interface drivers
* [ ] System services and units
* [ ] Physical hard disk partitions
* [ ] User authentication permissions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** System services and units
💡 `systemctl` is the control interface for systemd, managing services, targets, sockets, timers, and other units.

</details>

---

### 3. Most Linux system-wide service and application configuration files are conventionally stored in which directory?

* [ ] /bin
* [ ] /usr/bin
* [ ] /etc
* [ ] /dev

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc
💡 The `/etc` directory contains host-specific and system-wide configuration files.

</details>

---

### 4. An administrator wants to list all active systemd services currently running on the system. Which command provides the most accurate result?

* [ ] service --status-all
* [ ] systemctl list-units --type=service
* [ ] ps -aux
* [ ] ls /etc/systemd/

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl list-units --type=service
💡 This command lists active systemd service units and their current states.

</details>

---

### 5. The `/etc/fstab` file plays a critical role during system boot. What is its primary purpose?

* [ ] Managing firewall rules
* [ ] Defining disk mount points and options
* [ ] Configuring system services
* [ ] Tracking running processes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Defining disk mount points and options
💡 `/etc/fstab` specifies how and where filesystems are mounted during boot.

</details>

---

### 6. In systemd-based systems, which command ensures a service starts automatically at boot time?

* [ ] crontab
* [ ] init.d
* [ ] systemctl enable
* [ ] systemctl run

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl enable
💡 `enable` creates symbolic links so the service starts automatically during system boot.

</details>

---

### 7. What is the primary function of the `/etc/passwd` file in Linux?

* [ ] Storing login history
* [ ] Containing encrypted user passwords
* [ ] Listing user account information
* [ ] Logging sudo access attempts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Listing user account information
💡 `/etc/passwd` stores usernames, UIDs, GIDs, home directories, and shells (passwords are stored in `/etc/shadow`).

</details>

---

## 🔸 Intermediate (14 Questions)

---

### 8. Which command is used to display the current operational status of a systemd-managed service?

* [ ] service
* [ ] systemctl status
* [ ] svc status
* [ ] checkservice

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl status
💡 Displays service state, logs, PID, and recent execution details.

</details>

---

### 9. What is the primary purpose of the `/etc/systemd/system/` directory?

* [ ] Temporary configuration storage
* [ ] User-defined and overridden service unit files
* [ ] Storage of system logs
* [ ] Location of compiled binaries

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** User-defined and overridden service unit files
💡 This directory contains custom unit files and overrides that take precedence over defaults.

</details>

---

### 10. After modifying a systemd unit file, which command must be executed to reload systemd’s configuration database?

* [ ] reload-system
* [ ] systemctl reload
* [ ] systemctl daemon-reexec
* [ ] systemctl daemon-reload

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl daemon-reload
💡 Reloads unit files without restarting services.

</details>

---

### 11. What is the effect of executing `systemctl mask nginx.service`?

* [ ] Hides service output
* [ ] Prevents the service from being started by linking it to `/dev/null`
* [ ] Stops system logging
* [ ] Changes service execution priority

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevents the service from being started by linking it to `/dev/null`
💡 Masking ensures the service cannot be started manually or automatically.

</details>

---

### 12. Which file typically stores system-wide environment variables applicable to all users?

* [ ] /etc/environment
* [ ] /home/.env
* [ ] /etc/sysctl.conf
* [ ] /etc/bash.bashrc

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/environment
💡 It sets global environment variables without shell-specific syntax.

</details>

---

### 13. A `.service` file in systemd is best described as which type of file?

* [ ] Shell script
* [ ] Binary executable
* [ ] Unit configuration file
* [ ] Journal log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Unit configuration file
💡 It defines how a service is started, stopped, and managed.

</details>

---

### 14. The `chkconfig` command is primarily associated with which functionality?

* [ ] Managing systemd logs
* [ ] Installing packages
* [ ] Managing SysVinit runlevel services
* [ ] Displaying hardware details

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Managing SysVinit runlevel services
💡 `chkconfig` is used in legacy SysVinit-based systems.

</details>

---

### 15. Which command disables a systemd service from starting automatically at boot?

* [ ] systemctl off
* [ ] systemctl disable
* [ ] disable-service
* [ ] service disable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl disable
💡 Removes symbolic links used for auto-start at boot.

</details>

---

### 16. The `/etc/rc.d/` directory is traditionally used in which initialization system?

* [ ] BSD init
* [ ] SysVinit systems
* [ ] systemd
* [ ] Red Hat only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SysVinit systems
💡 Contains runlevel-specific startup scripts.

</details>

---

### 17. Which command displays all properties and low-level details of a systemd unit?

* [ ] systemctl help
* [ ] systemctl details
* [ ] systemctl show
* [ ] unitctl info

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl show
💡 Outputs detailed unit metadata in key-value format.

</details>

---

### 18. What is the primary purpose of the `journalctl` command?

* [ ] Start journaling filesystems
* [ ] View logs collected by systemd-journald
* [ ] Edit syslog configuration
* [ ] View service unit files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** View logs collected by systemd-journald
💡 `journalctl` queries binary logs maintained by systemd.

</details>

---

### 19. What information is stored in the `/etc/hostname` file?

* [ ] DNS server entries
* [ ] Static IP configuration
* [ ] System hostname
* [ ] Enabled services list

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** System hostname
💡 Defines the persistent hostname of the system.

</details>

---

### 20. Which configuration file defines filesystem mount options used during system startup?

* [ ] /etc/shadow
* [ ] /etc/fstab
* [ ] /etc/hosts
* [ ] /etc/profile

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/fstab
💡 Specifies mount points, filesystem types, and options.

</details>

---

### 21. How can a service reload its configuration without fully restarting in systemd (if supported)?

* [ ] systemctl refresh
* [ ] systemctl daemon-reload
* [ ] systemctl reload
* [ ] reloadctl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl reload
💡 Sends a reload signal to services that support dynamic reconfiguration.

</details>

---

## 🔺 Difficult (9 Questions)

---

### 22. Which systemd target corresponds to traditional SysVinit runlevel 5?

* [ ] graphical.target
* [ ] multi-user.target
* [ ] runlevel5.target
* [ ] gui.target

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** graphical.target
💡 Runlevel 5 maps to a multi-user system with GUI.

</details>

---

### 23. What is the immediate effect of executing `systemctl isolate multi-user.target`?

* [ ] Starts all background services
* [ ] Switches the system to a non-GUI, multi-user mode
* [ ] Terminates all logged-in users
* [ ] Reboots the system

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Switches the system to a non-GUI, multi-user mode
💡 Isolating a target stops unrelated units and activates only those required.

</details>

---

### 24. How can an administrator view logs related specifically to failed systemd services?

* [ ] systemctl --failed
* [ ] journalctl --failed
* [ ] systemctl status --failed
* [ ] systemctl error log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** journalctl --failed
💡 Displays logs associated with services that failed to start.

</details>

---

### 25. Which file should be modified to change system-wide shell behavior for all users upon login?

* [ ] /etc/bashrc
* [ ] /etc/bash.bashrc
* [ ] /etc/profile
* [ ] /etc/environment

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/profile
💡 `/etc/profile` configures global shell initialization for login shells.

</details>

---

### 26. What is the key distinction between `/etc/systemd/system/` and `/lib/systemd/system/`?

* [ ] One stores logs, the other stores binaries
* [ ] One is for user units, the other for system units
* [ ] `/lib` contains vendor defaults, `/etc` contains overrides and custom units
* [ ] There is no functional difference

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `/lib` contains vendor defaults, `/etc` contains overrides and custom units
💡 Units in `/etc` take precedence over `/lib`.

</details>

---

### 27. What is the primary purpose of a systemd `timer` unit?

* [ ] Setting service execution timeouts
* [ ] Scheduling service activation
* [ ] Logging system time
* [ ] Delaying system boot

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Scheduling service activation
💡 Timers replace cron for systemd-managed scheduling.

</details>

---

### 28. Which method correctly creates a custom systemd service unit?

* [ ] nano /etc/systemd/system/custom.service
* [ ] create-unit
* [ ] systemctl new-unit
* [ ] mkunit custom.service

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** nano /etc/systemd/system/custom.service
💡 Custom units are manually created in `/etc/systemd/system/`.

</details>

---

### 29. What is the function of the `ExecStartPre=` directive in a systemd service unit?

* [ ] Validates dependencies
* [ ] Executes commands before the main service starts
* [ ] Restarts the service on failure
* [ ] Reloads the service automatically

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Executes commands before the main service starts
💡 Often used for prerequisite checks or setup tasks.

</details>

---

### 30. What is the operational behavior of a service defined with `Type=oneshot`?

* [ ] Disables itself after execution
* [ ] Executes once and exits
* [ ] Runs continuously in the background
* [ ] Repeatedly reloads itself

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Executes once and exits
💡 Used for initialization or configuration tasks.

</details>

---

## **Session 11 : Linux OS**

---

### 1. A system administrator receives a report of a vulnerability in a critical Linux service. What is the **primary purpose of applying a software patch** in this context?

* [ ] To uninstall outdated software
* [ ] To add new user accounts
* [ ] To fix bugs or security vulnerabilities
* [ ] To create system backups

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To fix bugs or security vulnerabilities
💡 Patches are designed to correct software defects or vulnerabilities. Applying them ensures system security and stability. This aligns with standard Linux security practices (Red Hat Security Guide, Ubuntu Security Notices).

</details>

---

### 2. An administrator wants to apply a downloaded patch file to update a configuration file. Which command is **specifically designed for applying patches in Linux**?

* [ ] add
* [ ] patch
* [ ] update
* [ ] fix

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** patch
💡 The `patch` command reads a diff file (commonly ending in `.patch`) and applies the changes to the original files. `update` or `fix` do not handle patch files.

</details>

---

### 3. A developer shares a set of modifications in a text-based diff format. Which **file extension is conventionally used for such patch files**?

* [ ] .tar
* [ ] .zip
* [ ] .patch
* [ ] .conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .patch
💡 Patch files usually contain differences between files in a text format and conventionally use the `.patch` extension. `.tar` and `.zip` are archive formats; `.conf` is for configuration files.

</details>

---

### 4. A Linux server shows high CPU usage. Which tool **provides a real-time overview of system performance**, including CPU and memory usage?

* [ ] vi
* [ ] top
* [ ] grep
* [ ] df

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** top
💡 `top` displays real-time system resource usage including CPU, memory, and running processes, which is essential for performance monitoring. `df` shows disk usage, `vi` is a text editor, and `grep` searches text.

</details>

---

### 5. On a Linux system, where are most **X server configuration files stored**?

* [ ] /usr/local/bin
* [ ] /etc/X11/
* [ ] /var/log/
* [ ] /boot/

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/X11/
💡 `/etc/X11/` contains X server configuration files, including `xorg.conf`. `/usr/local/bin` is for executables, `/var/log/` is for logs, `/boot/` stores boot files.

</details>

---

### 6. A Linux administrator runs `startx` on a headless server. What **does this command accomplish**?

* [ ] Starts network services
* [ ] Launches the graphical user interface
* [ ] Starts the firewall
* [ ] Reboots the system

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Launches the graphical user interface
💡 `startx` initializes the X server and launches a desktop environment on Linux. It does not handle network, firewall, or system reboot.

</details>

---

### 7. To dynamically change display resolution on an active X server session, which **utility is typically used**?

* [ ] ifconfig
* [ ] xrandr
* [ ] netstat
* [ ] passwd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** xrandr
💡 `xrandr` allows administrators to query and modify display resolution, orientation, and output dynamically. `ifconfig` is for network interfaces, `netstat` for network connections, `passwd` for password management.

</details>

---

### 8. A developer wants to generate a patch from two versions of a source file for submission to a version control system. Which **command is used to create a patch file**?

* [ ] cmp
* [ ] diff
* [ ] grep
* [ ] sed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** diff
💡 `diff` compares files line by line and generates differences. Using `diff -u oldfile newfile > changes.patch` creates a patch. `cmp` only reports first difference, `grep` searches text, and `sed` edits streams.

</details>

---

### 9. Where is the **main X server configuration file** located in modern Linux distributions?

* [ ] /etc/x.conf
* [ ] /etc/X11/xorg.conf
* [ ] /etc/X11/xserver.cfg
* [ ] /usr/X11/config

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/X11/xorg.conf
💡 `xorg.conf` defines input devices, screens, monitors, and graphics drivers. Most modern distros can run X without this file, but it is still the standard configuration location.

</details>

---

### 10. An administrator wants to allow a specific user on a remote machine to access the X server. Which **command manages X server access control**?

* [ ] Connect to a remote server
* [ ] xhost
* [ ] Modify patch files
* [ ] View system logs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** xhost
💡 `xhost` grants or revokes access to the X server for remote hosts or users. It is not for connecting, editing patches, or log viewing.

</details>

---

### 11. A Debian-based server needs all packages updated to their latest versions. Which **command sequence ensures both package lists and installed packages are updated**?

* [ ] yum update
* [ ] dnf upgrade
* [ ] apt update && apt upgrade
* [ ] rpm install

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** apt update && apt upgrade
💡 `apt update` refreshes package lists, and `apt upgrade` installs available updates. `yum` and `dnf` are used in Red Hat-based systems, while `rpm install` only installs packages and does not handle dependencies.

</details>

---

### 12. A system administrator wants to quickly check **how long the system has been running and the current load**. Which command provides this information?

* [ ] uname -r
* [ ] uptime
* [ ] whoami
* [ ] free

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** uptime
💡 `uptime` displays the current time, how long the system has been running, the number of logged-in users, and the system load averages. `uname` shows kernel info, `whoami` the current user, `free` memory stats.

</details>

---

### 13. A system is experiencing performance issues. Which command gives a **summary of memory, CPU, and I/O statistics** for analysis?

* [ ] vmstat
* [ ] top
* [ ] iostat
* [ ] ps aux

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** vmstat
💡 `vmstat` reports virtual memory, processes, CPU, and I/O statistics over time, useful for system performance troubleshooting. `top` is real-time, `iostat` focuses on disk I/O, `ps aux` lists processes.

</details>

---

### 14. A patch file is being prepared for a critical source code fix. What does a **typical patch file contain**?

* [ ] Compiled binaries
* [ ] Source code differences
* [ ] Disk usage reports
* [ ] Shell scripts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Source code differences
💡 Patch files are text-based and contain line-by-line differences between old and new source code files, usually generated with `diff`. They do not contain binaries or system reports.

</details>

---

### 15. In a unified diff patch file, lines that **start with “+” indicate**:

* [ ] Comments
* [ ] Deletions
* [ ] Additions
* [ ] Errors

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Additions
💡 In unified diff format, `+` denotes lines to be added, `-` lines to be removed, and lines without prefixes remain unchanged.

</details>

---

### 16. A Linux system is running multiple graphical sessions. What is the **primary role of the Xorg process**?

* [ ] Web server
* [ ] Authentication service
* [ ] X Window System display server
* [ ] Background job scheduler

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** X Window System display server
💡 Xorg handles rendering graphical interfaces and managing input/output devices for the X Window System. It is not a web server, authentication service, or scheduler.

</details>

---

### 17. During system maintenance, which **type of file is most commonly patched**?

* [ ] User password
* [ ] Source code file
* [ ] Log file
* [ ] Swap partition

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Source code file
💡 Patches are applied to source code to fix bugs or add features. Passwords, logs, or swap partitions are not modified by patches.

</details>

---

### 18. To **verify whether an X server is currently running**, which command would you use?

* [ ] xstatus
* [ ] ps aux | grep X
* [ ] display-check
* [ ] systemctl status display

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ps aux | grep X
💡 Using `ps aux | grep X` lists processes matching “X,” confirming if the X server is active. `xstatus` and `display-check` are not standard commands.

</details>

---

### 19. A system administrator schedules automated backups every night. Which utility **enables task automation** in Linux?

* [ ] crontab
* [ ] GUI launchers
* [ ] ssh
* [ ] top

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** crontab
💡 `crontab` schedules recurring tasks. GUI launchers and `top` do not automate tasks, and `ssh` is for remote login.

</details>

---

### 20. To **check disk space usage** on a Linux filesystem, which command is appropriate?

* [ ] free
* [ ] df
* [ ] uname
* [ ] kill

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** df
💡 `df` reports free and used space on mounted filesystems. `free` is for memory, `uname` for system info, `kill` for terminating processes.

</details>

---

### 21. In enterprise Linux, which patch type allows **kernel updates without requiring a system reboot**?

* [ ] Static patch
* [ ] Live patch
* [ ] Dynamic mount
* [ ] Cold patch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Live patch
💡 Live patching (e.g., ksplice, kpatch) allows critical kernel fixes to be applied without downtime, reducing service disruption.

</details>

---

### 22. In an X server configuration, which section **specifies monitor settings** such as resolution and refresh rate?

* [ ] InputDevice
* [ ] Screen
* [ ] Monitor
* [ ] Display

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Monitor
💡 The `Monitor` section in `xorg.conf` defines display-specific parameters. `Screen` ties device and monitor together, `InputDevice` handles keyboard/mouse, `Display` is not a standard section.

</details>

---

### 23. What is the **effect of running `diff -u oldfile newfile`**?

* [ ] Updates the old file in place
* [ ] Produces a unified diff output
* [ ] Displays files recursively
* [ ] Merges source code automatically

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Produces a unified diff output
💡 `diff -u` creates a context-aware patch suitable for use with `patch`. It does not merge or overwrite files directly.

</details>

---

### 24. A production server uses livepatch. What is the **main benefit in enterprise environments**?

* [ ] Reduces disk usage
* [ ] Applies kernel updates without downtime
* [ ] Speeds up boot time
* [ ] Cleans up old files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Applies kernel updates without downtime
💡 Livepatch allows critical kernel fixes without rebooting, ensuring high availability, which is crucial in enterprise systems.

</details>

---

### 25. In `/etc/X11/xorg.conf`, which section **selects the graphics card driver**?

* [ ] Keyboard
* [ ] Device
* [ ] Monitor
* [ ] Screen

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Device
💡 The `Device` section specifies the graphics card and its driver. `Screen` ties monitor and device, `Monitor` defines display parameters, `Keyboard` is for input.

</details>

---

### 26. In modern Linux systems, which daemon **manages centralized system logging**?

* [ ] xlogd
* [ ] journald
* [ ] logrotate
* [ ] rsync

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** journald
💡 `systemd-journald` centralizes logs for system and applications. `logrotate` manages log rotation, `rsync` synchronizes files, `xlogd` is obsolete.

</details>

---

### 27. On GNOME desktops, which is the **default display manager** for handling graphical logins?

* [ ] SDDM
* [ ] LightDM
* [ ] GDM
* [ ] XDM

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** GDM
💡 GNOME Display Manager (GDM) provides graphical login services. SDDM is common in KDE, LightDM is lightweight, XDM is legacy.

</details>

---

### 28. After applying a patch, which command **verifies if it was applied correctly**?

* [ ] grep patch
* [ ] patch -R
* [ ] diff
* [ ] checkinstall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** diff
💡 Comparing the modified file against the intended result using `diff` confirms successful patch application. `patch -R` reverts, `grep patch` searches text, `checkinstall` manages packages.

</details>

---

### 29. What is the **role of `xinit`** in X server operation?

* [ ] Starts a text editor
* [ ] Initializes system services
* [ ] Launches an X server session
* [ ] Restarts display manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Launches an X server session
💡 `xinit` initializes an X server and starts a client session. It does not launch editors or restart the display manager.

</details>

---

### 30. In X server architecture, which **component is responsible for rendering graphics on the display**?

* [ ] xinput
* [ ] xfs
* [ ] X client
* [ ] X server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** X server
💡 The X server communicates with hardware and renders graphics based on instructions from X clients. `xinput` handles input devices, `xfs` is a filesystem, X clients request rendering but do not render themselves.

</details>

---
