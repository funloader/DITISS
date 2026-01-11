> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 04

## **Session 3 : Linux OS**

---

### 1. In Red Hat–based Linux distributions, which installer framework is responsible for handling disk partitioning, package selection, and Kickstart automation?

* [ ] Ubiquity
* [ ] YaST
* [ ] Anaconda
* [ ] Calamares

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Anaconda
💡 Anaconda is the default installer for RHEL, CentOS, Rocky Linux, and AlmaLinux, supporting GUI, text, and Kickstart-based automated installations.

</details>

---

### 2. During system startup, which Linux component is specifically responsible for loading the kernel into memory and transferring control to it?

* [ ] BIOS
* [ ] Shell
* [ ] Bootloader
* [ ] Kernel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bootloader
💡 The bootloader (e.g., GRUB2) loads the kernel and initramfs into memory and passes control to the kernel.

</details>

---

### 3. On most modern systems, which key is commonly used to access BIOS/UEFI firmware settings during boot?

* [ ] Esc
* [ ] F2
* [ ] Ctrl
* [ ] Tab

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** F2
💡 Although vendor-specific, **F2** is one of the most commonly used keys to access BIOS/UEFI settings.

</details>

---

### 4. What is the very first logical stage in the Linux boot process?

* [ ] Kernel initialization
* [ ] BIOS/UEFI firmware execution
* [ ] Init system startup
* [ ] Displaying the login prompt

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** BIOS/UEFI firmware execution
💡 BIOS/UEFI initializes hardware, performs POST, and locates the bootloader.

</details>

---

### 5. Which file format is universally used to distribute bootable Linux installation media?

* [ ] .txt
* [ ] .exe
* [ ] .iso
* [ ] .tar.gz

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .iso
💡 ISO images follow ISO-9660 standards and can be written directly to optical media or USB devices.

</details>

---

### 6. During Linux installation, which tools are commonly used for disk partitioning?

* [ ] Disk Manager
* [ ] fdisk
* [ ] parted
* [ ] Both b and c

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both b and c
💡 `fdisk` and `parted` are standard Linux partitioning tools supported by installers like Anaconda.

</details>

---

### 7. What is the primary function of a bootloader such as GRUB?

* [ ] Handles user authentication
* [ ] Loads the kernel into memory
* [ ] Manages network services
* [ ] Formats storage devices

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Loads the kernel into memory
💡 Bootloaders bridge firmware and the operating system by loading the kernel and initramfs.

</details>

---

## 🔸 Intermediate Level (Installation & Boot Mechanics)

---

### 8. After a Linux system is installed, which command is commonly used on Debian-based systems to install new packages?

* [ ] apt-get
* [ ] install
* [ ] linux-install
* [ ] package

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** apt-get
💡 `apt-get` interfaces with APT repositories to install, update, and manage packages.

</details>

---

### 9. Which file type enables a **fully automated, unattended installation** in Red Hat–based distributions?

* [ ] init.rc
* [ ] anaconda.cfg
* [ ] kickstart.cfg
* [ ] boot.cfg

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kickstart.cfg
💡 Kickstart files define installation parameters such as disks, packages, users, and networking.

</details>

---

### 10. In a Kickstart file, what is the purpose of the `%packages` section?

* [ ] Network configuration
* [ ] Package and package group selection
* [ ] Disk partitioning
* [ ] Bootloader installation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Package and package group selection
💡 `%packages` specifies individual RPMs or package groups to be installed.

</details>

---

### 11. What is the primary responsibility of `systemd` during the Linux boot process?

* [ ] Loading firmware
* [ ] Detecting hardware
* [ ] Managing system services and targets
* [ ] Formatting file systems

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Managing system services and targets
💡 `systemd` replaces traditional init systems and manages services, sockets, and dependencies.

</details>

---

### 12. Which of the following is **NOT** a Linux bootloader?

* [ ] GRUB
* [ ] LILO
* [ ] BCD
* [ ] ISOLINUX

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** BCD
💡 BCD (Boot Configuration Data) is used by Microsoft Windows, not Linux.

</details>

---

### 13. Where is the bootloader typically installed on modern systems?

* [ ] /boot/grub
* [ ] /root
* [ ] MBR or EFI System Partition
* [ ] /etc/init.d

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MBR or EFI System Partition
💡 Legacy systems use MBR; UEFI systems use the EFI System Partition (ESP).

</details>

---

### 14. Which Kickstart directive defines the root user’s password?

* [ ] %password
* [ ] %user
* [ ] rootpw
* [ ] loginpass

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** rootpw
💡 `rootpw` sets the root password, optionally in encrypted form.

</details>

---

### 15. To initiate a Kickstart-based installation, what must be done?

* [ ] Rename the file to initrd.img
* [ ] Reference it using a boot option
* [ ] Place it in /etc/init
* [ ] Embed it into the kernel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reference it using a boot option
💡 The installer must be pointed to the Kickstart file using the `ks=` boot parameter.

</details>

---

### 16. Which Linux command safely creates a bootable USB from an ISO image?

* [ ] cp image.iso /dev/sdb
* [ ] mkboot /dev/sdb
* [ ] dd if=image.iso of=/dev/sdX
* [ ] mkfs.iso /dev/usb

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dd if=image.iso of=/dev/sdX
💡 `dd` performs a block-level copy, preserving boot structures.

</details>

---

### 17. During boot, what is the main role of `initramfs`?

* [ ] Provide user login
* [ ] Mount the root filesystem
* [ ] Start application services
* [ ] Load graphical interfaces

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mount the root filesystem
💡 `initramfs` contains drivers and scripts needed to access the real root filesystem.

</details>

---

### 18. Which tool is used to verify the integrity of an ISO image before installation?

* [ ] df
* [ ] sha256sum
* [ ] lsblk
* [ ] du

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** sha256sum
💡 Hash verification ensures the ISO has not been corrupted or tampered with.

</details>

---

### 19. What does UEFI stand for?

* [ ] Unified Enhanced File Interface
* [ ] Unified Extensible Firmware Interface
* [ ] Universal EFI
* [ ] User Environment Firmware Integration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Unified Extensible Firmware Interface
💡 UEFI replaces legacy BIOS with modular, extensible firmware capabilities.

</details>

---

### 20. Which directory typically stores the Linux kernel image?

* [ ] /usr/bin
* [ ] /boot
* [ ] /var/log
* [ ] /etc/init

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /boot
💡 Kernel images such as `vmlinuz` and initramfs files reside in `/boot`.

</details>

---

### 21. Immediately after the bootloader executes, what is the next step?

* [ ] Kernel is loaded into memory
* [ ] systemd starts
* [ ] BIOS reinitializes
* [ ] Login screen appears

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kernel is loaded into memory
💡 Control is handed from the bootloader to the kernel.

</details>

---

## 🔺 Difficult Level (Enterprise & Automation Perspective)

---

### 22. Which Kickstart directive ensures **zero user interaction** during installation?

* [ ] interactive
* [ ] autopilot
* [ ] skip
* [ ] install

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** install
💡 `install` combined with proper Kickstart directives enforces non-interactive installation.

</details>

---

### 23. Which boot parameter correctly initiates a Kickstart installation from CD/DVD?

* [ ] kickstart=init.cfg
* [ ] ks=cdrom:/ks.cfg
* [ ] start=kick.cfg
* [ ] autoinstall=true

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ks=cdrom:/ks.cfg
💡 `ks=` is the standard kernel parameter for specifying Kickstart locations.

</details>

---

### 24. Which boot stage is responsible for detecting hardware and loading essential drivers required to access the root filesystem?

* [ ] BIOS
* [ ] initrd/initramfs
* [ ] GRUB
* [ ] Kernel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** initrd/initramfs
💡 initramfs bridges the gap between kernel loading and root filesystem mounting.

</details>

---

### 25. Which configuration file does GRUB2 dynamically generate and use?

* [ ] /boot/grub.conf
* [ ] /boot/grub/grub.cfg
* [ ] /etc/init.d/grub
* [ ] /etc/boot.cfg

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /boot/grub/grub.cfg
💡 `grub.cfg` is auto-generated and should not be edited manually.

</details>

---

### 26. On Debian-based systems, which command regenerates GRUB configuration files?

* [ ] grub-update
* [ ] grub2
* [ ] update-grub
* [ ] bootctl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** update-grub
💡 `update-grub` scans kernels and updates `grub.cfg`.

</details>

---

### 27. What is a major advantage of using LVM during Linux installation?

* [ ] Fixed partition sizes
* [ ] Dynamic resizing and snapshots
* [ ] Automatic encryption
* [ ] Faster kernel loading

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamic resizing and snapshots
💡 LVM enables flexible storage management without repartitioning.

</details>

---

### 28. Which Anaconda boot option forces a **text-based installation mode**?

* [ ] text-mode
* [ ] anaconda-cli
* [ ] inst.text
* [ ] console-install

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** inst.text
💡 `inst.text` is used in minimal or headless installation environments.

</details>

---

### 29. Which GRUB2 feature allows booting multiple operating systems from a single system?

* [ ] chainloader
* [ ] bootctl
* [ ] autoload
* [ ] initram

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chainloader
💡 Chainloading passes control to another bootloader, commonly used in dual-boot setups.

</details>

---

### 30. Why are headless installation methods preferred in large enterprise environments?

* [ ] Rich graphical interfaces
* [ ] Reduced automation
* [ ] Scalable and consistent deployments
* [ ] Manual configuration control

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Scalable and consistent deployments
💡 Automated, headless installations ensure uniform system builds across data centers.

</details>

---

## **Session 3 & 4 : Linux OS**

---

### 1. An administrator wants to directly inspect the final GRUB2 boot menu configuration that the system actually uses during startup. Which file should be examined?

* [ ] /etc/grub.conf
* [ ] /boot/grub/grub.cfg
* [ ] /etc/grub.d/grub.cfg
* [ ] /root/grub.cfg

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /boot/grub/grub.cfg
💡 This is the autogenerated GRUB2 configuration file parsed at boot time. It should not be edited manually.

</details>

---

### 2. After modifying GRUB defaults on a Debian-based system, which command regenerates the GRUB2 configuration?

* [ ] grub-install
* [ ] grub-reload
* [ ] update-grub
* [ ] grub-update

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** update-grub
💡 `update-grub` is a wrapper around `grub-mkconfig` used in Debian-based systems.

</details>

---

### 3. During the Linux boot process, why is initramfs required before mounting the root filesystem?

* [ ] To initialize the graphical environment
* [ ] To load essential drivers needed to access the root filesystem
* [ ] To configure package repositories
* [ ] To update installed software

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To load essential drivers needed to access the root filesystem
💡 initramfs contains critical modules (storage, filesystem drivers) required early in boot.

</details>

---

### 4. Which underlying package format is natively managed by Red Hat–based Linux distributions?

* [ ] dpkg
* [ ] rpm
* [ ] apt
* [ ] yum

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** rpm
💡 RPM is the package format; YUM/DNF are higher-level package managers built on RPM.

</details>

---

### 5. An administrator downloads a standalone `.deb` file and wants to install it manually. Which command should be used?

* [ ] rpm -i
* [ ] dpkg -i
* [ ] yum install
* [ ] pacman -S

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dpkg -i
💡 `dpkg -i` installs Debian packages without resolving dependencies automatically.

</details>

---

### 6. In traditional SysV init systems, what does a run level represent?

* [ ] A kernel boot parameter
* [ ] A bootloader configuration state
* [ ] A predefined system state based on active services
* [ ] A filesystem mount type

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A predefined system state based on active services
💡 Each run level defines which services are started or stopped.

</details>

---

### 7. Which SysV run level represents multi-user mode with networking enabled but without a graphical interface?

* [ ] 1
* [ ] 3
* [ ] 5
* [ ] 0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 3
💡 Run level 3 is full multi-user mode with networking but no GUI.

</details>

---

## 🔸 Intermediate (14 MCQs)

---

### 8. Which GRUB2 file contains the dynamically generated menu entries displayed during boot?

* [ ] /boot/grub2/menu.lst
* [ ] /boot/grub/grub.cfg
* [ ] /etc/init.d/grub
* [ ] /etc/default/grub

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /boot/grub/grub.cfg
💡 This file is generated from scripts in `/etc/grub.d/` and settings in `/etc/default/grub`.

</details>

---

### 9. What type of content is primarily stored inside an initrd/initramfs image?

* [ ] Bootloader binaries
* [ ] A complete Linux root filesystem
* [ ] Kernel modules required to mount the root filesystem
* [ ] Firmware and BIOS tables

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kernel modules required to mount the root filesystem
💡 It enables access to disks using LVM, RAID, or encrypted partitions.

</details>

---

### 10. Which mechanism has largely replaced SysV run levels in modern Linux distributions?

* [ ] Upstart
* [ ] systemd targets
* [ ] CRON
* [ ] SELinux

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemd targets
💡 systemd uses targets like `multi-user.target` and `graphical.target`.

</details>

---

### 11. Which command displays the current and previous run level on SysV-based systems?

* [ ] systemctl
* [ ] runlevel
* [ ] chkconfig
* [ ] ps

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** runlevel
💡 It shows the previous and current run levels.

</details>

---

### 12. What is the function of the command `rpm -qa`?

* [ ] Displays RPM version
* [ ] Lists all installed RPM packages
* [ ] Installs a package
* [ ] Removes an installed package

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lists all installed RPM packages
💡 `-q` queries and `-a` selects all installed packages.

</details>

---

### 13. Which Debian command safely adds an external repository along with its signing key?

* [ ] yum enable-repo
* [ ] add-apt-repository
* [ ] rpm --add-repo
* [ ] apt-import

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** add-apt-repository
💡 It updates APT sources and handles repository metadata.

</details>

---

### 14. What is the primary role of the `/etc/default/grub` file?

* [ ] Stores GRUB menu entries
* [ ] Defines system run levels
* [ ] Configures GRUB behavior and parameters
* [ ] Manages kernel modules

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configures GRUB behavior and parameters
💡 It controls timeout, default OS, kernel parameters, etc.

</details>

---

### 15. Which utility actually generates the `grub.cfg` file from templates and scripts?

* [ ] grub2-mkconfig
* [ ] grub-builder
* [ ] init-grub
* [ ] update-initramfs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** grub2-mkconfig
💡 It parses `/etc/grub.d/` and `/etc/default/grub`.

</details>

---

### 16. What is the fundamental responsibility of the init (PID 1) process?

* [ ] Upgrading the kernel
* [ ] Initializing and supervising system services
* [ ] Displaying the boot menu
* [ ] Disk partitioning

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Initializing and supervising system services
💡 init/systemd is the first user-space process.

</details>

---

### 17. In Debian-based systems, which command removes a package along with its configuration files?

* [ ] apt purge
* [ ] dpkg uninstall
* [ ] rpm --remove
* [ ] apt clean

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** apt purge
💡 `purge` removes binaries as well as configuration files.

</details>

---

### 18. What is the effect of running `systemctl isolate graphical.target`?

* [ ] Boots into recovery mode
* [ ] Reboots the system
* [ ] Switches to CLI multi-user mode
* [ ] Switches the system to GUI mode

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Switches the system to GUI mode
💡 `graphical.target` includes display manager and GUI services.

</details>

---

### 19. Why is the GRUB timeout parameter important?

* [ ] Controls kernel logging delay
* [ ] Specifies reboot delay
* [ ] Determines how long the boot menu waits for user input
* [ ] Sets network initialization delay

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Determines how long the boot menu waits for user input
💡 Configured via `GRUB_TIMEOUT` in `/etc/default/grub`.

</details>

---

### 20. Which command regenerates the initramfs image in Ubuntu?

* [ ] mkinitrd
* [ ] grub2-mkimage
* [ ] update-initramfs
* [ ] update-grub

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** update-initramfs
💡 Used after kernel or driver changes.

</details>

---

### 21. What information does the `yum repolist` command provide?

* [ ] Deletes repositories
* [ ] Lists enabled YUM repositories
* [ ] Installs all repo packages
* [ ] Displays repository configuration files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lists enabled YUM repositories
💡 Useful for troubleshooting package availability.

</details>

---

## 🔺 Difficult (9 MCQs)

---

### 22. Which GRUB2 script is primarily responsible for detecting installed Linux kernels?

* [ ] 00_header
* [ ] 10_linux
* [ ] 40_custom
* [ ] 05_defaults

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 10_linux
💡 It automatically generates menu entries for Linux kernels.

</details>

---

### 23. Which tool installs a `.deb` package while automatically resolving dependencies?

* [ ] dpkg -i
* [ ] apt install
* [ ] gdebi package.deb
* [ ] rpm -i

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** gdebi package.deb
💡 `gdebi` resolves dependencies for local `.deb` files.

</details>

---

### 24. How is the GRUB2 configuration regenerated on RHEL-based systems?

* [ ] grub2-update
* [ ] grub2-mkconfig -o /boot/grub2/grub.cfg
* [ ] update-grub
* [ ] grub-setup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** grub2-mkconfig -o /boot/grub2/grub.cfg
💡 RHEL does not use `update-grub`.

</details>

---

### 25. Which services are typically included in `multi-user.target`?

* [ ] Display manager and GUI services
* [ ] Network, SSH, and text-based login services
* [ ] X server only
* [ ] Emergency recovery shell

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network, SSH, and text-based login services
💡 Equivalent to SysV run level 3.

</details>

---

### 26. Which file defines APT repository sources in Debian systems?

* [ ] /etc/apt.conf
* [ ] /etc/apt/sources.list
* [ ] /etc/apt/repos.conf
* [ ] /usr/lib/apt/repositories

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/apt/sources.list
💡 Additional sources may exist in `/etc/apt/sources.list.d/`.

</details>

---

### 27. Which GRUB2 module enables support for Logical Volume Manager (LVM)?

* [ ] lvm
* [ ] lvm_support
* [ ] grub_lvm
* [ ] grubfs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** lvm
💡 Required to boot systems installed on LVM volumes.

</details>

---

### 28. What is the purpose of the `rpm -V` command?

* [ ] Validates package signatures
* [ ] Verifies integrity of installed files
* [ ] Updates RPM packages
* [ ] Lists trusted repositories

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Verifies integrity of installed files
💡 It checks size, permissions, hashes, and ownership.

</details>

---

### 29. Which command reveals the default boot target in a systemd-based system?

* [ ] runlevel
* [ ] who -r
* [ ] systemctl get-default
* [ ] chkconfig

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl get-default
💡 Shows whether the system boots into graphical or multi-user mode.

</details>

---

### 30. Why is initramfs packaged as a compressed CPIO archive?

* [ ] Only to reduce disk usage
* [ ] To allow easy manual modification
* [ ] To enable efficient loading by the kernel during early boot
* [ ] To replace the GRUB configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To enable efficient loading by the kernel during early boot
💡 The kernel natively understands CPIO archives.

</details>

---
