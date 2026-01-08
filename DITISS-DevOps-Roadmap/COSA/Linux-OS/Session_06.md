## 🌐🔐 **Session 6 – Networking, OpenSSH, VNC & Network Authentication (PG-DITISS)**

---

## 🔹 **1. Concept Overview**

Session 6 focuses on **network addressing**, **secure remote communication**, **remote GUI access**, and **authentication mechanisms** in Linux:

* **IPv4 & IPv6 addressing**
* **OpenSSH for secure CLI access**
* **VNC for remote GUI access**
* **Network authentication basics**
* **Lab:** Network configuration, OpenSSH, VNC setup

> Content strictly aligned with **COSA-Linux.pdf** and PG-DITISS exam expectations.

---

## 📘 **2. Key Definitions**

* **IP Address:** Logical identifier assigned to a network interface.
* **IPv4:** 32-bit IP addressing scheme (decimal, dotted format).
* **IPv6:** 128-bit IP addressing scheme (hexadecimal).
* **OpenSSH:** Secure protocol for encrypted remote login and file transfer.
* **VNC:** Virtual Network Computing – remote desktop sharing protocol.
* **Authentication:** Process of verifying user identity on a network.

---

## 🧩 **3. Main Content (Organized from COSA Notes)**

---

### 🌍 **A. Network Addressing – IPv4 & IPv6**

#### 🔹 IPv4 Addressing

* **Size:** 32-bit
* **Format:** Dotted decimal (e.g., `192.168.1.10`)
* **Total addresses:** ~4.3 billion
* **Common Classes (Exam-Oriented):**

| Class | Range                     | Usage           |
| ----- | ------------------------- | --------------- |
| A     | 1.0.0.0 – 126.0.0.0       | Large networks  |
| B     | 128.0.0.0 – 191.255.0.0   | Medium networks |
| C     | 192.0.0.0 – 223.255.255.0 | Small networks  |

**Private IPv4 Ranges (MCQ Favorite):**

* `10.0.0.0 – 10.255.255.255`
* `172.16.0.0 – 172.31.255.255`
* `192.168.0.0 – 192.168.255.255`

---

#### 🔹 IPv6 Addressing

* **Size:** 128-bit
* **Format:** Hexadecimal, colon-separated
  Example: `2001:0db8:85a3::8a2e:0370:7334`
* **Advantages:**

  * Larger address space
  * No NAT required
  * Better security support

**Exam One-liner:**
👉 *IPv6 replaces IPv4 due to address exhaustion.*

---

### 🔐 **B. Using OpenSSH for Network Communication**

(from COSA: Secure remote access concepts)

#### 🔹 What is OpenSSH?

* Open-source implementation of **SSH (Secure Shell)**
* Provides **encrypted communication** over insecure networks

#### 🔹 Common OpenSSH Services

* `sshd` – SSH daemon (server)
* `ssh` – Client utility

#### 🔹 Key SSH Commands

| Command                    | Purpose              |
| -------------------------- | -------------------- |
| `ssh user@host`            | Remote login         |
| `scp file user@host:/path` | Secure copy          |
| `sftp user@host`           | Secure file transfer |

**Default Port:** `22`

**Exam Note:**

* SSH replaces **Telnet** (unencrypted)

---

### 🖥️ **C. Using VNC for Network Communication**

#### 🔹 What is VNC?

* **Graphical remote access protocol**
* Allows remote desktop sharing over a network

#### 🔹 Features

* Platform-independent
* Works on **client-server model**
* Uses TCP ports (e.g., `5901`, `5902`)

#### 🔹 Use Case

* Remote GUI access to Linux servers
* Preferred when **GUI required**

**Comparison (MCQ Trap):**

| SSH       | VNC                      |
| --------- | ------------------------ |
| CLI-based | GUI-based                |
| Encrypted | Not encrypted by default |
| Port 22   | Port 5900+               |

---

### 🔑 **D. Network Authentication**

(from COSA: User & security basics)

#### 🔹 Authentication Methods

* **Password-based authentication**
* **Key-based authentication (SSH keys)**
* **Centralized authentication (conceptual):**

  * LDAP
  * NIS
  * Kerberos (awareness level)

#### 🔹 SSH Key-Based Authentication

* Uses **public-private key pair**
* More secure than passwords
* Eliminates password-based login

**Exam Keyword:**
👉 *Key-based authentication = stronger security*

---

## 📌 **4. Important Facts / Points for MCQs**

* IPv4 = 32-bit, IPv6 = 128-bit
* SSH port = **22**
* VNC uses ports starting from **5900**
* SSH is encrypted, Telnet is not
* IPv6 written in hexadecimal
* SSH supports key-based authentication

---

## 🧪 **5. Examples**

* Check IP address:

  ```bash
  ip addr
  ```
* SSH login:

  ```bash
  ssh user@192.168.1.10
  ```
* Start VNC session:

  ```bash
  vncserver
  ```

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* ❌ IPv6 is NOT backward compatible with IPv4
* ❌ VNC is NOT secure by default
* ⚠️ SSH ≠ FTP (FTP is unencrypted)
* ⚠️ Private IPs are NOT routable on internet
* ⚠️ VNC ≠ RDP (Windows)

---


