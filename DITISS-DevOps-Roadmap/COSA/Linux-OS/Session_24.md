## 📊 Session 24: Logging & Monitoring Using Script

---

## 🧠 **1. Concept Overview**

* **Logging** records system/application events for troubleshooting and auditing.
* **Monitoring** checks system health and performance in real time.
* Using **Bash scripts**, admins can **automate log collection, analysis, alerts, and reporting**.
* PG-DITISS focus: **commands, log locations, scripting logic, redirection, and MCQ traps**.

---

## 📘 **2. Key Definitions**

* **Log File:** Text file storing system or application events.
* **Monitoring:** Continuous observation of system resources/services.
* **syslog:** Standard Linux logging mechanism.
* **rsyslog:** Enhanced syslog daemon (default in most Linux distros).
* **Alert:** Notification when a threshold/event occurs.

---

## 🧩 **3. Main Content (Organized & Exam-Oriented)**

---

## 🗂️ **A. Linux Logging Basics**

### 🔹 Common Log Files (Very Important)

| Log File            | Purpose                         |
| ------------------- | ------------------------------- |
| `/var/log/messages` | General system logs             |
| `/var/log/syslog`   | System activity (Debian/Ubuntu) |
| `/var/log/auth.log` | Authentication logs             |
| `/var/log/secure`   | Security logs (RHEL/CentOS)     |
| `/var/log/dmesg`    | Kernel messages                 |
| `/var/log/boot.log` | Boot process logs               |

📌 **MCQ Fact:**

* Logs are generally stored in **`/var/log`**

---

### 🔹 Logging Services

* **rsyslog** → Collects and manages logs
* **journalctl** → systemd journal logs

```bash
systemctl status rsyslog
journalctl -xe
```

---

## 🧪 **B. Logging Using Bash Script**

### 🔹 Why Script-Based Logging?

* Custom logs
* Automated entries
* Centralized tracking

---

### 🔹 Simple Logging Script

```bash
#!/bin/bash
echo "$(date) : Script executed" >> /var/log/custom.log
```

📌 **MCQ Trap:**

* `>>` appends logs; `>` overwrites logs

---

### 🔹 Logging Command Output

```bash
df -h >> /var/log/disk.log 2>&1
```

📌 **Key Point:**

* `2>&1` redirects **errors to output**

---

## 📈 **C. Monitoring Using Bash Script**

### 🔹 What to Monitor?

* Disk usage
* CPU load
* Memory usage
* Service status
* Log errors

---

### 🔹 Disk Usage Monitoring Example

```bash
#!/bin/bash
df -h | grep /dev/sda1 >> /var/log/disk_usage.log
```

---

### 🔹 CPU & Memory Monitoring

```bash
top -b -n1 | head -5 >> /var/log/cpu.log
free -m >> /var/log/memory.log
```

---

### 🔹 Service Monitoring

```bash
systemctl is-active apache2
```

```bash
if ! systemctl is-active apache2
then
  echo "Apache down" >> /var/log/service.log
fi
```

📌 **MCQ Fact:**

* `systemctl is-active` checks service state

---

## ⏰ **D. Automating Monitoring with Cron**

```bash
crontab -e
```

Example:

```bash
*/5 * * * * /root/monitor.sh
```

📌 **MCQ Trap:**

* Cron jobs use **non-interactive shell**

---

## 🎯 **4. Important Facts / Points for MCQs**

* Logs stored in `/var/log`
* `rsyslog` manages system logs
* `journalctl` works with systemd
* `>>` used for log append
* Monitoring scripts often run via **cron**
* STDERR FD = **2**

---

## 💡 **5. Examples**

* Login failure monitoring via `/var/log/auth.log`
* Disk alert when usage > 80%
* Apache service uptime monitoring
* Custom application logs

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* Logging ≠ Monitoring
* `>` vs `>>` confusion
* `tail -f` ≠ static log view
* `journalctl` ≠ `/var/log/messages`
* Cron environment ≠ user shell
* Log rotation handled by **logrotate**, not scripts

---

📌 **One-Line Exam Memory Aid:**

> **Logging = Record events | Monitoring = Observe system health**
