# 🐧 **Title:** Introduction to Linux, Linux File System & Basic Administration Commands

### 🎓 *(PG-DITISS – Session 1 & 2)*

---

## 🧠 1. Concept Overview

Linux is an **open-source, Unix-like operating system** based on the **Linux Kernel**, widely used in **servers, desktops, embedded systems, and cloud environments**.
It supports **multi-user, multitasking**, strong **security**, and **powerful command-line tools**, making it essential for PG-DITISS.

---

## 📘 2. Key Definitions

* **Linux Kernel:** Core component managing CPU, memory, devices, processes
* **Linux Distribution (Distro):** Kernel + utilities + libraries (e.g., Ubuntu, Debian, Fedora)
* **Shell:** Command interpreter (e.g., bash) that interfaces between user and kernel
* **Root (/):** Topmost directory in Linux file system
* **CLI:** Command Line Interface
* **GUI:** Graphical User Interface
* **File Descriptor:** Integer representing open files (0-stdin, 1-stdout, 2-stderr)

---

## 📚 3. Main Content (Organized from Notes)

---

### 🐧 A. Introduction to Linux

* Developed by **Linus Torvalds (1991)**
* Licensed under **GNU General Public License (GPL)**
* **Everything is a file** (files, directories, devices)
* Used in:

  * Servers, supercomputers
  * Embedded devices
  * Android OS (Linux kernel based)

#### ✅ Advantages

* Open source & free
* High stability & performance
* Multi-user & multitasking
* Strong security model
* Large community support

#### ❌ Disadvantages

* Steeper learning curve
* Limited drivers for some hardware

---

### 🏗️ B. Linux Architecture

| Component        | Function                     |
| ---------------- | ---------------------------- |
| Kernel           | Core OS, resource management |
| Shell            | User interface to kernel     |
| System Libraries | OS functionalities           |
| System Utilities | Admin & user tools           |
| Hardware         | CPU, RAM, Disk               |

---

### 🌳 C. Linux File System

* **Hierarchical tree structure**
* Starts from root `/`
* No drive letters (unlike Windows)

#### 📂 Important Directories

| Directory | Purpose               |
| --------- | --------------------- |
| /         | Root directory        |
| /home     | User home directories |
| /bin      | Essential binaries    |
| /sbin     | System binaries       |
| /etc      | Configuration files   |
| /dev      | Device files          |
| /proc     | Process info          |
| /var      | Logs, variable data   |
| /tmp      | Temporary files       |
| /boot     | Boot loader files     |

---

### 📄 D. Types of Files

1. **Regular files:** text, binary
2. **Directory files:** containers
3. **Device files:** `/dev/sda1`, `/dev/cdrom`

---

### 💾 E. Linux File Systems (Storage)

| File System | Key Point                       |
| ----------- | ------------------------------- |
| ext2        | No journaling                   |
| ext3        | Journaling, backward compatible |
| ext4        | Default, large file support     |
| XFS         | High-performance                |
| Btrfs       | Snapshot, fault tolerance       |
| Swap        | Virtual memory                  |

---

### 📁 F. Working with Files & Directories (Commands)

#### 🚶 Navigation

* `pwd` – present working directory
* `cd`, `cd ..`, `cd /`, `cd ~`

#### 📃 Listing

* `ls`, `ls -l`, `ls -a`, `ls -al`

#### 📄 File Operations

* `cp` – copy
* `mv` – move/rename
* `rm` – delete file
* `touch` – create empty file
* `file` – detect file type

#### 📂 Directory Operations

* `mkdir` – create directory
* `rmdir` – delete empty directory

---

### 🔍 G. File Viewing & Text Processing

| Command     | Use                  |
| ----------- | -------------------- |
| cat         | Display file         |
| tac         | Reverse display      |
| more / less | Paged view           |
| head / tail | First/last lines     |
| wc          | Word/line/byte count |
| sort        | Sort content         |
| grep        | Pattern search       |
| diff        | Compare files        |

---

### 🔐 H. File Permissions & Access Control

#### 🔑 Permission Types

* **r** – read
* **w** – write
* **x** – execute

#### 👥 Ownership

* User (u)
* Group (g)
* Others (o)

#### 👀 Viewing Permissions

```bash
ls -l
```

Example: `-rwxr-xr--`

---

### 🛠️ I. chmod Command

#### 🔢 Numeric Mode

| Value | Permission |
| ----- | ---------- |
| 7     | rwx        |
| 6     | rw-        |
| 5     | r-x        |
| 4     | r--        |

Example:

```bash
chmod 764 file
```

#### 🔣 Symbolic Mode

```bash
chmod u+x file
chmod g-w file
chmod o=r file
```

---

### 👤 J. chown & chgrp

* Change ownership:

```bash
chown user file
chown user:group file
```

* Change group:

```bash
chgrp group file
```

---

### 🌐 K. Network Commands

| Command | Purpose                 |
| ------- | ----------------------- |
| telnet  | Remote login (insecure) |
| ftp     | File transfer           |
| sftp    | Secure FTP              |
| ssh     | Secure shell            |
| finger  | User information        |

---

### 🖴 L. Secondary Storage Devices

* Devices represented as files under `/dev`
* Examples:

  * Hard disk: `/dev/sda`
  * CDROM: `/dev/cdrom`

#### ⚙️ Common Operations

* Mounting: `mount /dev/sda1 /mnt`
* Unmounting: `umount /mnt`
* Formatting: `mkfs.ext4 /dev/sdb1`

---

## 📝 4. Important Facts / Points for MCQs

* Linux is **case-sensitive**
* Root directory is `/`
* File descriptors: **0-stdin, 1-stdout, 2-stderr**
* Execute permission on directory = ability to **enter directory**
* `rm` does NOT ask confirmation
* `mv` used for both **move & rename**
* `chmod 777` = full permission to everyone (security risk)

---

## 🧪 5. Examples

* Absolute path: `/home/user/Documents`
* Relative path: `Documents`
* Hidden file: `.bashrc`
* Soft link: `ln -s file link`
* Hard link: `ln file link`

---

## 🎯 6. MCQ Pointers / Exam Traps

* **Linux vs Ubuntu:** Linux = kernel, Ubuntu = distribution
* **Execute on directory ≠ execute file**
* **rm vs rmdir:** rmdir only deletes empty directories
* **chmod numeric vs symbolic** often confused
* `>` overwrites, `>>` appends
* `ls -a` shows hidden files
* `file` checks content, NOT extension
* `swap ≠ filesystem for storage`

---

