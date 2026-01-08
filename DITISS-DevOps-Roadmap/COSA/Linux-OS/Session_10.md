## ⚙️📂 **Session 10 – Services Management & System Configuration Files (PG-DITISS)**

---

## 🔹 **1. Concept Overview**

Session 10 focuses on **managing system services** and **understanding critical Linux configuration files**, both **highly testable in MCQs and lab viva**:

* Service management (SysVinit & systemd basics)
* Important system configuration files
* **NIS (Network Information Service) – concept & configuration**
* **Lab:** Working with config files, NIS configuration

> Content strictly aligned with **COSA-Linux.pdf** and PG-DITISS syllabus scope.

---

## 📘 **2. Key Definitions**

* **Service (Daemon):** Background process providing system/network functionality.
* **systemd:** Modern init system for service management.
* **SysVinit:** Traditional init system using run levels.
* **Configuration File:** Text file controlling system/service behavior.
* **NIS:** Network Information Service for centralized user management.

---

## 🧩 **3. Main Content (Organized from COSA Notes)**

---

### ⚙️ **A. Services Management in Linux**

Linux services run as **daemon processes**.

#### 🔹 Common Services

* `sshd` – Secure Shell
* `cups` – Printing service
* `network` – Network service
* `nfs` – Network File System

---

#### 🔹 Service Management Commands

##### ▶ SysVinit (Legacy – MCQ-Oriented)

| Command                | Purpose                |
| ---------------------- | ---------------------- |
| `service name start`   | Start service          |
| `service name stop`    | Stop service           |
| `service name restart` | Restart service        |
| `chkconfig`            | Enable/disable at boot |

---

##### ▶ systemd (Modern)

| Command                     | Purpose         |
| --------------------------- | --------------- |
| `systemctl start service`   | Start service   |
| `systemctl stop service`    | Stop service    |
| `systemctl restart service` | Restart service |
| `systemctl enable service`  | Enable at boot  |
| `systemctl status service`  | Service status  |

**Exam Note:**
👉 *systemctl is replacement for service + chkconfig*

---

### 📂 **B. System Configuration Files**

Linux uses **plain text configuration files**.

#### 🔹 Important System Config Files (MCQ Favorite)

| File               | Purpose                |
| ------------------ | ---------------------- |
| `/etc/passwd`      | User account info      |
| `/etc/shadow`      | Encrypted passwords    |
| `/etc/group`       | Group information      |
| `/etc/fstab`       | Filesystem mount info  |
| `/etc/hosts`       | Hostname to IP mapping |
| `/etc/resolv.conf` | DNS configuration      |
| `/etc/sysconfig/`  | Service configs (RHEL) |

**Exam One-liner:**
👉 *Most Linux configurations are done by editing files in `/etc`.*

---

### 🔐 **C. NIS (Network Information Service)**

#### 🔹 What is NIS?

* Centralized authentication system
* Shares:

  * User accounts
  * Groups
  * Hostnames
* Works on **client-server model**

#### 🔹 NIS Components

| Component  | Role                          |
| ---------- | ----------------------------- |
| NIS Server | Maintains user/group database |
| NIS Client | Queries server for info       |
| NIS Domain | Logical grouping              |

---

#### 🔹 NIS Configuration Files

* `/etc/yp.conf`
* `/etc/sysconfig/network`
* `/etc/nsswitch.conf`

**Exam Keyword:**
👉 *NIS centralizes user authentication*

---

## 📌 **4. Important Facts / Points for MCQs**

* Services run as daemons
* systemctl used in systemd systems
* `/etc/fstab` controls auto-mount
* `/etc/nsswitch.conf` controls name resolution order
* NIS is centralized authentication
* NIS uses client-server architecture

---

## 🧪 **5. Examples**

* Check service status:

  ```bash
  systemctl status sshd
  ```
* Enable service at boot:

  ```bash
  systemctl enable cups
  ```
* Edit config file:

  ```bash
  vi /etc/hosts
  ```

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* ❌ systemd ≠ SysVinit
* ❌ NIS ≠ LDAP (different services)
* ⚠️ Editing wrong config file may break service
* ⚠️ `/etc/fstab` syntax errors can stop boot
* ⚠️ Services must be **enabled** to start at boot

---

