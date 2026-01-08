## 🐧 **Session 3 & 4 – Linux Installation, Boot Process & Package Management (PG-DITISS)**

---

## 🔹 **1. Concept Overview**

These sessions cover:

* **Linux installation methods**
* **Boot process & boot loader (GRUB)**
* **Initial RAM Disk (initrd/initramfs)**
* **Run levels / targets**
* **Repository & package management (RPM & DEB)**
* **Lab focus:** Installation, Boot Loader configuration, Yellow Dog Updater (YUM)

> Content aligned with **COSA-Linux.pdf** and **PG-DITISS exam orientation**

---

## 📘 **2. Key Definitions**

* **Linux Distribution:** OS packaged with Linux kernel + utilities (e.g., Ubuntu, Fedora).
* **Anaconda Installer:** Graphical/text-based Linux installer (mainly Red Hat-based).
* **Boot Loader:** Program that loads OS kernel into memory (e.g., GRUB).
* **GRUB:** Grand Unified Bootloader, default Linux boot loader.
* **initrd/initramfs:** Temporary root filesystem loaded into RAM during boot.
* **Run Level:** Defines system operational state (SysVinit).
* **Repository:** Storage location of software packages.
* **Package Manager:** Tool to install/update/remove software (RPM, DEB).

---

## 🧩 **3. Main Content (Organized)**

### 🛠️ **A. Installation of Linux**

(from COSA: Linux Distributions & Installation basics)

**Pre-requisites:**

* ISO image of Linux distribution
* Bootable USB/DVD
* Disk partitions (/, /boot, swap, /home)

**Common Installation Steps:**

1. Boot from installation media
2. Select language & keyboard
3. Disk partitioning
4. Package selection
5. Boot loader installation
6. User & root configuration
7. Reboot

---

### 🖥️ **B. Interactive Anaconda Installer**

(Used in **RHEL / CentOS / Fedora**)

**Features:**

* GUI-based installer
* Supports:

  * Disk partitioning (manual/automatic)
  * Network configuration
  * Software selection
* Uses **Kickstart** for automation

**Exam Note:**
Anaconda ≠ Ubuntu installer (Ubuntu uses **Ubiquity / Subiquity**)

---

### 🤖 **C. Hands-Free Installation (Automated)**

**Kickstart Installation**

* Configuration file contains:

  * Disk layout
  * Packages
  * Network settings
* Used for **mass deployment**
* No user interaction during install

**MCQ Keyword:** *Kickstart = Automated Linux installation*

---

### ⚙️ **D. Understanding the Linux Boot Procedure**

(from COSA: Boot & Kernel concepts)

**Boot Sequence (Exam Favorite):**

| Step | Component          | Description             |
| ---- | ------------------ | ----------------------- |
| 1    | BIOS / UEFI        | Hardware initialization |
| 2    | MBR / EFI          | Locates boot loader     |
| 3    | GRUB               | Loads kernel            |
| 4    | Kernel             | Initializes hardware    |
| 5    | initrd/initramfs   | Loads drivers           |
| 6    | init/systemd       | Starts services         |
| 7    | Run level / Target | User environment        |

---

### 🚀 **E. Configuring the GRUB Boot Loader**

(from COSA: Boot Loader references)

* **GRUB config file:**

  * `/boot/grub/grub.cfg`
* Allows:

  * OS selection
  * Kernel parameters
  * Recovery mode
* Supports:

  * Dual boot
  * Password protection

**GRUB Commands (MCQ):**

* `grub-install`
* `update-grub`

---

### 🧠 **F. Initial RAM Disk (initrd / initramfs)**

* Temporary filesystem loaded into RAM
* Contains:

  * Essential drivers
  * Mount tools
* Used **before actual root filesystem mounts**

**Exam One-liner:**
*initrd helps kernel mount root filesystem*

---

### 🔁 **G. Understanding Run Levels**

(SysVinit – Exam-oriented)

| Run Level | Meaning          |
| --------- | ---------------- |
| 0         | Halt             |
| 1         | Single-user mode |
| 3         | Multi-user (CLI) |
| 5         | Multi-user (GUI) |
| 6         | Reboot           |

> Modern systems use **systemd targets**, but PG-DITISS still asks run levels.

---

### 📦 **H. Repository & Package Management (RPM & DEB)**

(from COSA: Package Management & Commands)

#### 🔹 RPM-Based Systems (RHEL, CentOS, Fedora)

* Package format: `.rpm`
* Tool:

  * `rpm`
  * `yum` (Yellow Dog Updater Modified)

**YUM Features:**

* Automatic dependency resolution
* Uses repositories

**Commands:**

* `yum install pkg`
* `yum update`
* `yum remove`

---

#### 🔹 DEB-Based Systems (Ubuntu, Debian)

* Package format: `.deb`
* Tools:

  * `dpkg`
  * `apt / apt-get`

**Commands:**

* `apt-get install pkg`
* `apt-get update`
* `apt-get remove pkg`

---

## 📌 **4. Important Facts / Points for MCQs**

* Linux boot loader = **GRUB**
* Anaconda used in **Red Hat-based Linux**
* initrd loaded **before root filesystem**
* Run level 3 = CLI, Run level 5 = GUI
* RPM ≠ DEB
* YUM works on **RPM packages**
* Kickstart = automated installation

---

## 🧪 **5. Examples**

* Installing Apache:

  * RPM system: `yum install httpd`
  * DEB system: `apt-get install apache2`
* Switching run level:

  * `init 3` (CLI)
  * `init 5` (GUI)

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* ❌ Anaconda ≠ Ubuntu installer
* ❌ YUM is NOT for DEB packages
* ❌ initrd is NOT permanent filesystem
* ⚠️ GRUB config file location often confused
* ⚠️ Run levels vs systemd targets
* ⚠️ rpm does NOT resolve dependencies (yum does)

---
