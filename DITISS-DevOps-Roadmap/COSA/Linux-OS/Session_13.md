## 🛠️🌐📁 **Session 13 – Configuring Services, NFS & FTP Server (PG-DITISS)**

---

## 🔹 **1. Concept Overview**

Session 13 introduces **service configuration in Linux** with focus on **file-sharing services**, a **high-utility admin + MCQ topic**:

* Basics of configuring network services
* **NFS (Network File System) server setup**
* **FTP (File Transfer Protocol) server basics**
* **Lab:** NFS server configuration

> Content strictly aligned with **COSA-Linux.pdf** and PG-DITISS syllabus scope.

---

## 📘 **2. Key Definitions**

* **Service:** Background process (daemon) providing functionality.
* **NFS:** Network File System – allows file sharing over a network.
* **FTP:** File Transfer Protocol – used for file transfer.
* **Export:** Directory shared via NFS.
* **Daemon:** Background service process.

---

## 🧩 **3. Main Content (Organized from COSA Notes)**

---

### ⚙️ **A. Introduction to Configuring Services**

#### 🔹 General Steps to Configure Any Service

1. Install required package
2. Edit configuration file
3. Start service
4. Enable service at boot
5. Verify service

**Exam One-liner:**
👉 *Linux services are controlled using systemctl/service commands.*

---

### 📁 **B. Setting Up an NFS Server**

#### 🔹 What is NFS?

* Network File System
* Enables **file sharing between Linux systems**
* Client-server architecture

**Default Port:** 2049

---

#### 🔹 NFS Components

| Component  | Role                    |
| ---------- | ----------------------- |
| NFS Server | Exports directories     |
| NFS Client | Mounts remote directory |
| Export     | Shared directory        |

---

#### 🔹 Important NFS Configuration File (MCQ Favorite)

* `/etc/exports`

**Example Entry:**

```text
/shared 192.168.1.0/24(rw,sync)
```

---

#### 🔹 Common NFS Export Options

| Option           | Meaning             |
| ---------------- | ------------------- |
| `rw`             | Read/Write          |
| `ro`             | Read-only           |
| `sync`           | Synchronous writes  |
| `no_root_squash` | Root access allowed |

**Exam Trap:**
⚠️ `no_root_squash` = security risk

---

### 📥 **C. Setting Up an FTP Server (Conceptual)**

#### 🔹 What is FTP?

* File Transfer Protocol
* Used to upload/download files
* Client-server model

**Default Ports:**

* Control: 21
* Data: 20

#### 🔹 FTP Server Software

* vsftpd (Very Secure FTP Daemon)

**Exam One-liner:**
👉 *FTP is unencrypted by default.*

---

### 🔐 **D. NFS vs FTP (MCQ Comparison)**

| Feature    | NFS             | FTP             |
| ---------- | --------------- | --------------- |
| Purpose    | File sharing    | File transfer   |
| Encryption | No (by default) | No (by default) |
| Mountable  | Yes             | No              |
| OS usage   | Linux/UNIX      | Cross-platform  |

---

## 📌 **4. Important Facts / Points for MCQs**

* NFS config file = `/etc/exports`
* NFS port = **2049**
* FTP control port = **21**
* vsftpd = FTP server
* NFS uses client-server model
* Export = shared directory

---

## 🧪 **5. Examples**

* Start NFS service:

  ```bash
  systemctl start nfs
  ```
* Export directories:

  ```bash
  exportfs -r
  ```
* Mount NFS share:

  ```bash
  mount server:/shared /mnt
  ```

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* ❌ NFS ≠ Samba
* ❌ FTP ≠ SFTP
* ⚠️ no_root_squash allows root access
* ⚠️ FTP transmits passwords in plain text
* ⚠️ NFS is mainly for Linux systems

---

