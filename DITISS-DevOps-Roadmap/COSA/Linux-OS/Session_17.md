## 📌 Session 17 – Performance Tuning, Maintenance & Security (PG-DITISS – COSA) ⚙️🛡️

---

## ⚙️ **1️⃣ Introduction to Performance Tuning** 🚀

### 🔹 **Concept Overview**

* **Performance Tuning** = Optimizing system resources to achieve **maximum efficiency**
* Focuses on **CPU, Memory, Disk I/O, Network**
* Goal: **High throughput, low latency, system stability**

---

### 📘 **Key Definitions**

* **Throughput:** Amount of work done per unit time
* **Latency:** Time delay in response
* **Bottleneck:** Resource limiting system performance
* **Load Average:** Average system workload (1, 5, 15 min)

---

### 📚 **Main Content**

#### 🔸 **Performance Areas**

* **CPU:** Process scheduling, utilization
* **Memory:** RAM usage, cache, swap
* **Disk I/O:** Read/write speed
* **Network:** Bandwidth, packet loss

#### 🔸 **Common Monitoring Commands**

| Command   | Purpose                       |
| --------- | ----------------------------- |
| `top`     | Real-time process & CPU usage |
| `htop`    | Enhanced top                  |
| `vmstat`  | Memory & CPU stats            |
| `iostat`  | Disk I/O stats                |
| `free -m` | Memory usage                  |
| `uptime`  | Load average                  |

---

### 📌 **Important Facts / Points for MCQs**

* Load average > CPU cores → **Overloaded**
* High swap usage → **Low RAM**
* I/O wait indicates disk bottleneck
* Linux uses **page cache** aggressively

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ High CPU always bad → ❌ (can be normal)
* ✔ Swap ≠ bad (excessive swap is bad)
* ✔ Cache memory is **reclaimable**
* ✔ Load ≠ CPU utilization

---

### 🔧 **Corrections / Improvements**

* Tuning should be **data-driven**, not assumption-based
* Always monitor **before and after** changes

---

---

## 🛠️ **2️⃣ Maintenance and Troubleshooting** 🔍

### 🔹 **Concept Overview**

* **Maintenance:** Preventive actions to keep system healthy
* **Troubleshooting:** Identifying & fixing system issues

---

### 📘 **Key Definitions**

* **Preventive Maintenance:** Regular checks & updates
* **Corrective Maintenance:** Fix after failure
* **Log Files:** System activity records

---

### 📚 **Main Content**

#### 🔸 **Routine Maintenance Tasks**

* OS updates & patches
* Disk cleanup
* Log rotation
* Backup verification
* User & permission audit

#### 🔸 **Important Log Files**

| Log File            | Purpose                  |
| ------------------- | ------------------------ |
| `/var/log/syslog`   | General system logs      |
| `/var/log/messages` | Kernel & system messages |
| `/var/log/auth.log` | Authentication logs      |
| `/var/log/dmesg`    | Boot & hardware messages |

#### 🔸 **Troubleshooting Approach**

1. Identify symptoms
2. Check logs
3. Check resource usage
4. Verify configuration
5. Apply fix
6. Test & document

---

### 📌 **Important Facts / Points for MCQs**

* Logs are primary troubleshooting tools
* `dmesg` shows kernel messages
* Restart ≠ permanent fix
* Backup before major changes

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Delete logs blindly → ❌
* ✔ Use `logrotate` for logs
* ✔ Permissions cause many issues
* ✔ Configuration errors are common root cause

---

### 🔧 **Corrections / Improvements**

* Use **systemctl status** before restart
* Maintain **change logs** in production

---

---

## 🛡️ **3️⃣ The Threat Model and Protection Methods** 🔐

### 🔹 **Concept Overview**

* **Threat Model** identifies:

  * Assets
  * Threats
  * Vulnerabilities
  * Attack vectors
* Helps design **appropriate security controls**

---

### 📘 **Key Definitions**

* **Threat:** Potential cause of harm
* **Vulnerability:** Weakness in system
* **Attack Vector:** Method used to exploit vulnerability
* **Risk:** Threat × Vulnerability × Impact

---

### 📚 **Main Content**

#### 🔸 **Common Threats**

* Malware
* Unauthorized access
* Data leakage
* Denial of Service (DoS)
* Insider threats

#### 🔸 **Protection Methods**

| Layer   | Protection            |
| ------- | --------------------- |
| System  | Patching, hardening   |
| Network | Firewall, IDS         |
| User    | Strong authentication |
| Data    | Encryption, backups   |

#### 🔸 **Linux Security Tools**

* `iptables` / `ufw` → Firewall
* SELinux / AppArmor → Mandatory Access Control
* SSH keys → Secure access
* Audit logs → Accountability

---

### 📌 **Important Facts / Points for MCQs**

* Security is **layered (Defense in Depth)**
* Root account is highest risk
* Least privilege principle is critical
* Logs are security evidence

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Antivirus alone is sufficient → ❌
* ✔ Firewalls don’t stop insider attacks
* ✔ Encryption protects data at rest & transit
* ✔ Disabling unused services improves security

---

## 🎯 **Rapid MCQ Revision Summary (Session 17)** ✅

* Performance tuning → Optimize CPU, RAM, Disk, Network
* Load average ≠ CPU usage
* Logs are first step in troubleshooting
* Maintenance prevents downtime
* Threat model = Asset + Threat + Vulnerability
* Security uses **defense-in-depth**

---
