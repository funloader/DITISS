## 🧩🐧 **Session 5 – Shutdown, Kickstart & User Administration (PG-DITISS)**

---

## 🔹 **1. Concept Overview**

Session 5 focuses on:

* **System shutdown & reboot concepts**
* **Kickstart configuration and customization**
* **Automated deployment using Kickstart**
* **User administration in Linux**
* **Lab focus:** Package installation, Kickstart setup, user management

> Content strictly aligned with **COSA-Linux.pdf** and **PG-DITISS exam pattern**

---

## 📘 **2. Key Definitions**

* **Shutdown:** Graceful stopping of Linux system services and power-off/reboot.
* **Reboot:** Restarting the system without powering off.
* **Kickstart:** Automated Linux installation using a predefined configuration file.
* **Deployment:** Installing Linux on multiple systems using automation.
* **User Administration:** Managing users, groups, and permissions in Linux.

---

## 🧩 **3. Main Content (Organized from COSA Notes)**

---

### 🔌 **A. Shutdown & Installation Concepts**

Linux provides commands to **safely stop or restart** the system to prevent data loss.

#### 🔹 Common Shutdown Commands

| Command           | Purpose                 |
| ----------------- | ----------------------- |
| `shutdown -h now` | Halt system immediately |
| `shutdown -r now` | Reboot system           |
| `poweroff`        | Turn off power          |
| `reboot`          | Restart system          |
| `init 0`          | Shutdown (SysVinit)     |
| `init 6`          | Reboot (SysVinit)       |

**Important Exam Note:**

* Shutdown must be **graceful** to avoid filesystem corruption.
* Root privileges required.

---

### 🤖 **B. Kickstart Configuration & Customization**

Kickstart enables **hands-free Linux installation**.

#### 🔹 Kickstart Configuration File

* File name: `ks.cfg`
* Used by **Anaconda installer**
* Contains predefined installation instructions

#### 🔹 Key Sections in Kickstart File (MCQ-Oriented)

* Language & keyboard
* Installation source
* Disk partitioning
* Network configuration
* Package selection
* Root password
* Post-install scripts

**Exam Keyword:**
👉 *Kickstart = Automated installation for Red Hat-based systems*

---

### 🚀 **C. Deployment Using Kickstart**

**Purpose:**

* Install Linux on **multiple systems**
* No manual intervention

**Deployment Methods:**

* Bootable media (USB/DVD)
* Network-based (PXE)

**Advantages (Exam-Focused):**

* Saves time
* Standardized installations
* Reduces human error

---

### 👤 **D. User Administration (Linux Users & Groups)**

(from COSA: User & Group Management)

#### 🔹 Types of Users

1. **Root User**

   * Superuser
   * UID = 0
2. **Regular User**

   * Limited privileges
3. **Service User**

   * Used by services (apache, ftp, mail)

---

#### 🔹 User Management Commands

| Command            | Function            |
| ------------------ | ------------------- |
| `useradd username` | Create user         |
| `passwd username`  | Set/change password |
| `usermod`          | Modify user         |
| `userdel username` | Delete user         |
| `id username`      | Show UID/GID        |
| `whoami`           | Current user        |

---

#### 🔹 Group Management Commands

| Command                 | Function             |
| ----------------------- | -------------------- |
| `groupadd groupname`    | Create group         |
| `groupdel groupname`    | Delete group         |
| `usermod -g group user` | Change primary group |
| `groups user`           | Show user groups     |

---

#### 🔹 Important Files (MCQ Favorite)

* `/etc/passwd` → User account info
* `/etc/shadow` → Encrypted passwords
* `/etc/group` → Group info

---

## 📌 **4. Important Facts / Points for MCQs**

* Kickstart used with **Anaconda**
* Kickstart file = `ks.cfg`
* Root user UID = **0**
* `/etc/shadow` stores encrypted passwords
* Shutdown requires root access
* `init 0` = shutdown, `init 6` = reboot
* Service users improve **security**

---

## 🧪 **5. Examples**

* Create a user:

  ```bash
  useradd tom
  passwd tom
  ```
* Add user to group:

  ```bash
  usermod -aG developers tom
  ```
* Shutdown system:

  ```bash
  shutdown -h now
  ```

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* ❌ Kickstart is NOT for Ubuntu
* ❌ `/etc/passwd` does NOT store passwords
* ⚠️ `reboot` ≠ `shutdown -h`
* ⚠️ Root user ≠ Administrator (Windows)
* ⚠️ userdel does NOT delete home directory by default

---

