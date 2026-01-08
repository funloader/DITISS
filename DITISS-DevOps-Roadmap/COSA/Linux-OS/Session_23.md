## 🤖 Session 23: Automate Tasks Using Bash Script & Security Patches

---

## 🧠 **1. Concept Overview**

* **Automation** in Linux is achieved using **Bash shell scripts** to reduce manual effort.
* **Security patches** are critical updates that fix vulnerabilities in OS and software.
* In PG-DITISS, focus is on:

  * **Why & how automation is done**
  * **Patch management basics**
  * **Commands, concepts, and MCQ traps**

---

## 📖 **2. Key Definitions**

* **Automation:** Running tasks automatically using scripts or schedulers.
* **Bash Script:** A text file containing Linux commands executed sequentially.
* **Patch:** A piece of code that fixes bugs or security vulnerabilities.
* **Patch Management:** Process of applying, testing, and maintaining patches.
* **Package Manager:** Tool to install/update software (`apt`, `yum`, `dnf`).

---

## 🧩 **3. Main Content (MCQ-Oriented & Exam-Friendly)**

---

## ⚙️ **A. Automate Tasks Using Bash Script**

### 🔹 Why Automation?

* Reduces human error
* Saves time
* Ensures consistency
* Useful for repetitive system tasks

---

### 🔹 Common Tasks Automated Using Bash

* User creation
* Backup
* Log cleanup
* Service monitoring
* Disk usage alert
* Package updates

---

### 🔹 Basic Structure of Bash Script

```bash
#!/bin/bash
# Comments
commands
```

📌 **MCQ Fact:**

* Script must have **execute permission** (`chmod +x`)

---

### 🔹 Example: Simple Automation Script

```bash
#!/bin/bash
date >> /var/log/script.log
```

---

### 🔹 Scheduling Automation (cron)

* `cron` is used for **time-based job scheduling**

```bash
crontab -e
```

| Field | Meaning |
| ----- | ------- |
| *     | minute  |
| *     | hour    |
| *     | day     |
| *     | month   |
| *     | weekday |

📌 **MCQ Trap:**

* Cron runs with **limited environment variables**

---

## 🔐 **B. Security Patches**

---

### 🔹 What are Security Patches?

* Fix known vulnerabilities
* Prevent unauthorized access
* Improve system stability

---

### 🔹 Types of Patches

* Security patches
* Bug fixes
* Feature updates

---

### 🔹 Patch Management Process

1. Identify vulnerabilities
2. Test patches
3. Apply patches
4. Verify system
5. Rollback if required

---

### 🔹 Patch Installation Commands

* **Debian/Ubuntu**

```bash
sudo apt update
sudo apt upgrade
```

* **RHEL/CentOS**

```bash
sudo yum update
```

📌 **MCQ Fact:**

* `update` refreshes package list
* `upgrade` installs patches

---

### 🔹 Automated Patch Management

* Use **cron + script**
* Use tools:

  * `unattended-upgrades`
  * `yum-cron`

---

## 🎯 **4. Important Facts / Points for MCQs**

* Bash automation requires **execute permission**
* Cron jobs run as **specific user**
* Security patches reduce **attack surface**
* Package manager verifies **dependencies**
* Kernel patch may require **reboot**
* Patch ≠ Upgrade

---

## 💡 **5. Examples**

* Disk usage alert script
* Daily backup automation
* Weekly patch update via cron

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* Automation ≠ Manual execution
* Cron ≠ at (event-based)
* Patch ≠ Full OS reinstall
* Patch failure can cause **service downtime**
* Test patches before production
* `apt upgrade` ≠ `apt full-upgrade`

---

📌 **Quick Exam Memory Aid:**

> **Automation = Script + Scheduler**
> **Security = Regular Patch Management**
