## 📌 Session 18 – Service Security, Logging, NTP & DNS Security (PG-DITISS – COSA) 🔐🖧

---

## 🛡️ **1️⃣ Basic Service Security** 🔑

### 🔹 **Concept Overview**

* Securing Linux services ensures **confidentiality, integrity, and availability**
* Focus on **minimizing attack surface** and **proper configuration**
* Applies to: Web servers, Mail servers, FTP, SSH, etc.

---

### 📘 **Key Definitions**

* **Service:** A background process providing functionality
* **Daemon:** Another term for Linux service
* **Least Privilege:** Services run with minimum necessary permissions
* **Hardening:** Process of securing a system/service

---

### 📚 **Main Content**

#### 🔸 **Service Security Best Practices**

* Disable **unused services**

```bash
systemctl disable service_name
```

* Run services as **non-root users** when possible
* Regularly **update software packages**
* Restrict **network access** via firewall
* Enable **SELinux/AppArmor** policies
* Limit login attempts (e.g., `fail2ban` for SSH)

#### 🔸 **Monitoring Services**

* Check status:

```bash
systemctl status service_name
```

* Check running ports:

```bash
ss -tulnp
```

---

### 📌 **Important Facts / Points for MCQs**

* Unused services are a **common attack vector**
* Firewalls + service-level restrictions reduce risk
* SELinux/AppArmor enforces **mandatory access control**
* Non-root execution is key for security

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ All services must run as root → ❌ Wrong
* ✔ Disable services not needed
* ✔ Firewall doesn’t replace patching
* ✔ Logs help detect misuse

---

### 🔧 **Corrections / Improvements**

* Use **systemctl mask** for critical services
* Combine **audit + monitoring** for real-time detection

---

## 📝 **2️⃣ Logging and NTP** ⏱️

### 🔹 **Concept Overview**

* **Logging:** Collects system & service events
* **NTP:** Network Time Protocol ensures **accurate system time**
* Accurate timestamps are critical for:

  * Log analysis
  * Troubleshooting
  * Security audits

---

### 📘 **Key Definitions**

* **Syslog:** Standard logging protocol
* **rsyslog:** Linux syslog implementation
* **NTP:** Synchronizes system clock with time servers
* **Chrony:** Modern alternative to ntpd

---

### 📚 **Main Content**

#### 🔸 **Logging Basics**

* Main directories:

  * `/var/log/`
  * `/var/log/syslog` → General messages
  * `/var/log/auth.log` → Authentication
  * `/var/log/kern.log` → Kernel messages
* Commands:

```bash
tail -f /var/log/syslog
journalctl -xe
```

* Log rotation via **logrotate**

#### 🔸 **NTP Configuration**

* Install NTP:

```bash
sudo apt install ntp
```

* Configure servers in `/etc/ntp.conf`:

```conf
server 0.pool.ntp.org
server 1.pool.ntp.org
```

* Start service:

```bash
sudo systemctl start ntp
sudo systemctl enable ntp
```

---

### 📌 **Important Facts / Points for MCQs**

* Correct system time ensures **event correlation**
* Logs are essential for **auditing & troubleshooting**
* NTP default port → **UDP 123**

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ NTP ≠ security protocol
* ✔ Log rotation prevents disk full issues
* ✔ Chrony preferred for virtualized systems

---

### 🔧 **Corrections / Improvements**

* Modern systems use **systemd-timesyncd** for time sync
* Combine logs with **centralized logging** (ELK stack / Graylog)

---

## 🌐 **3️⃣ BIND and DNS Security** 🖧🔐

### 🔹 **Concept Overview**

* **BIND** (Berkeley Internet Name Domain) → Most common DNS server in Linux
* DNS security ensures:

  * Integrity of DNS records
  * Protection from spoofing or cache poisoning
* DNS attacks affect **network reliability & trust**

---

### 📘 **Key Definitions**

* **Zone File:** Stores DNS records for a domain
* **DNSSEC:** DNS Security Extensions to validate responses
* **TSIG:** Transaction SIGnature for secure zone transfers
* **Cache Poisoning:** Malicious injection of wrong DNS info

---

### 📚 **Main Content**

#### 🔸 **BIND Security Measures**

* Disable recursion for external queries

```conf
allow-recursion { localnets; };
```

* Restrict zone transfers

```conf
allow-transfer { master_ip; };
```

* Enable **DNSSEC**

```bash
dnssec-enable yes;
dnssec-validation yes;
```

* Run BIND as **non-root user (`named`)**
* Logging BIND events:

```conf
logging {
  channel default_file { file "/var/log/named/named.log"; };
  category default { default_file; };
};
```

#### 🔸 **Service Control**

```bash
sudo systemctl start bind9
sudo systemctl enable bind9
```

---

### 📌 **Important Facts / Points for MCQs**

* BIND port → **UDP/TCP 53**
* DNSSEC protects against **spoofing**
* Restrict zone transfers to **authorized servers only**
* Non-root execution reduces attack surface

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ DNS ≠ mail server
* ✔ Recursive queries externally → vulnerability
* ✔ Cache poisoning → security risk
* ✔ Logs are essential for troubleshooting

---

## 🎯 **Rapid MCQ Revision Summary (Session 18)** ✅

| Topic                  | Key Points                            | Ports / Files             |
| ---------------------- | ------------------------------------- | ------------------------- |
| Basic Service Security | Disable unused services, run non-root | `systemctl`, `ss -tulnp`  |
| Logging                | Syslog, logrotate, journald           | `/var/log/`, `journalctl` |
| NTP                    | Accurate time, NTP/Chrony             | UDP 123                   |
| BIND Security          | DNSSEC, restrict zone transfers       | UDP/TCP 53, `/etc/bind/`  |

---
