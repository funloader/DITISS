## 🌐📛 **Session 12 – Configuration of DNS (PG-DITISS)**

---

## 🔹 **1. Concept Overview**

Session 12 focuses on **DNS (Domain Name System) configuration in Linux**, a **very important networking + services topic** for:

* MCQs (concepts, files, records)
* Lab execution (DNS server & client setup)
* Viva questions

> Content strictly aligned with **COSA-Linux.pdf** and PG-DITISS syllabus scope.

---

## 📘 **2. Key Definitions**

* **DNS:** Domain Name System – translates domain names into IP addresses.
* **Domain Name:** Human-readable name (e.g., `www.google.com`).
* **IP Address:** Numeric network identifier.
* **Name Server:** Server that resolves DNS queries.
* **Zone:** Portion of DNS namespace managed by a server.
* **BIND:** Berkeley Internet Name Domain – most common DNS server software in Linux.

---

## 🧩 **3. Main Content (Organized from COSA Notes)**

---

### 🌐 **A. What is DNS & Why It Is Needed**

* Converts **hostname → IP address**
* Eliminates need to remember IP addresses
* Works on **client-server architecture**

**Exam One-liner:**
👉 *DNS is a distributed, hierarchical naming system.*

---

### 🏗️ **B. DNS Architecture**

#### 🔹 DNS Components

| Component  | Description                   |
| ---------- | ----------------------------- |
| DNS Client | Sends name resolution request |
| DNS Server | Resolves and replies          |
| Zone File  | Stores DNS records            |
| Resolver   | Library used by client        |

---

### 📦 **C. DNS Server in Linux (BIND)**

* Most common DNS software: **BIND**
* Service name: `named`
* Configuration directory: `/etc/named/`

---

### 📂 **D. Important DNS Configuration Files (MCQ Favorite)**

| File               | Purpose                  |
| ------------------ | ------------------------ |
| `/etc/named.conf`  | Main DNS configuration   |
| `/var/named/`      | Zone files location      |
| `/etc/resolv.conf` | DNS client configuration |
| `/etc/hosts`       | Local name resolution    |

**Exam Trap:**
❌ `/etc/hosts` ≠ DNS server
⚠️ It is checked **before DNS** (as per `nsswitch.conf`)

---

### 🗂️ **E. DNS Zones**

(from COSA)

#### 🔹 Types of Zones

1. **Forward Lookup Zone**

   * Name → IP
2. **Reverse Lookup Zone**

   * IP → Name

---

### 🧾 **F. Common DNS Record Types (Very Important for MCQs)**

| Record | Purpose         |
| ------ | --------------- |
| A      | Hostname → IPv4 |
| AAAA   | Hostname → IPv6 |
| PTR    | IP → Hostname   |
| NS     | Name server     |
| MX     | Mail server     |
| CNAME  | Alias name      |

**Exam One-liner:**
👉 *A record maps domain name to IPv4 address.*

---

### ⚙️ **G. DNS Configuration Workflow (Lab-Oriented)**

1. Install BIND
2. Configure `/etc/named.conf`
3. Create zone files
4. Start DNS service (`named`)
5. Configure client `/etc/resolv.conf`
6. Test using `nslookup` / `dig`

---

## 📌 **4. Important Facts / Points for MCQs**

* DNS uses **port 53**
* Protocol: **UDP (mostly)**, TCP for zone transfer
* DNS server software = **BIND**
* Service name = `named`
* Forward zone ≠ Reverse zone
* `/etc/resolv.conf` used by DNS client

---

## 🧪 **5. Examples**

* Check DNS service:

  ```bash
  systemctl status named
  ```
* DNS client config:

  ```bash
  nameserver 192.168.1.1
  ```
* Test DNS:

  ```bash
  nslookup www.example.com
  ```

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* ❌ DNS ≠ DHCP
* ❌ MX record is NOT for name resolution
* ⚠️ PTR record used in reverse lookup
* ⚠️ `/etc/hosts` overrides DNS
* ⚠️ named is daemon, not config file

---

