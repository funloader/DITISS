## 📌 Session 14 – Linux Networking Services (PG-DITISS – COSA) 🖧

---

## 🧩 **1️⃣ The Samba Server: Networking with Windows Systems** 🪟🔗

### 🔹 **Concept Overview**

* **Samba** is an **open-source implementation of SMB/CIFS protocol**
* Enables **file & printer sharing** between **Linux and Windows systems**
* Allows Linux to act as:

  * File Server
  * Print Server
  * Windows Domain Member / Controller (basic)

---

### 📘 **Key Definitions**

* **SMB (Server Message Block):** Network file-sharing protocol used by Windows
* **CIFS:** Enhanced version of SMB
* **Samba Daemons:**

  * `smbd` → File & printer sharing
  * `nmbd` → NetBIOS name resolution
* **Workgroup:** Logical Windows network grouping

---

### 📚 **Main Content**

#### 🔸 **Samba Components**

* `smb.conf` → Main configuration file (`/etc/samba/smb.conf`)
* `smbd` → Handles file sharing & authentication
* `nmbd` → Handles browsing & NetBIOS

#### 🔸 **Basic Samba Installation**

```bash
sudo apt install samba
```

#### 🔸 **Starting / Enabling Samba**

```bash
sudo systemctl start smbd
sudo systemctl enable smbd
```

#### 🔸 **Creating a Samba Share**

* Add at end of `smb.conf`:

```ini
[shared]
path = /home/share
browseable = yes
writable = yes
guest ok = yes
```

#### 🔸 **Samba User Management**

```bash
sudo smbpasswd -a username
```

---

### 📌 **Important Facts for MCQs**

* Protocol used: **SMB/CIFS**
* Default config file: **/etc/samba/smb.conf**
* Windows access format: `\\Linux_IP\sharename`
* Samba ≠ FTP (file sharing vs file transfer)

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Samba ≠ NFS (NFS is Unix-Unix)
* ❌ `nmbd` ≠ file sharing (only name resolution)
* ✔ Samba works on **TCP ports 139 & 445**
* ✔ Samba allows Linux to integrate into Windows network

---

### 🔧 **Corrections / Improvements**

* Modern systems rely more on **SMB2/SMB3** instead of CIFS
* Domain Controller role is **limited** compared to Windows AD

---

---

## 🧩 **2️⃣ Configuring a DHCP Server** 📡

### 🔹 **Concept Overview**

* **DHCP (Dynamic Host Configuration Protocol)** automatically assigns:

  * IP Address
  * Subnet Mask
  * Gateway
  * DNS Server
* Eliminates **manual IP configuration**

---

### 📘 **Key Definitions**

* **DHCP Lease:** Time period for IP validity
* **Scope:** Range of IP addresses
* **Reservation:** Fixed IP for a MAC address
* **Server Port:** UDP 67 (server), UDP 68 (client)

---

### 📚 **Main Content**

#### 🔸 **DHCP Package**

```bash
sudo apt install isc-dhcp-server
```

#### 🔸 **Main Configuration File**

* `/etc/dhcp/dhcpd.conf`

#### 🔸 **Basic DHCP Configuration Example**

```conf
subnet 192.168.1.0 netmask 255.255.255.0 {
  range 192.168.1.100 192.168.1.200;
  option routers 192.168.1.1;
  option domain-name-servers 8.8.8.8;
}
```

#### 🔸 **Start DHCP Service**

```bash
sudo systemctl start isc-dhcp-server
```

---

### 📌 **Important Facts for MCQs**

* DHCP works on **UDP**
* Automatically assigns **network parameters**
* Centralized IP management
* DHCP ≠ DNS (IP assignment vs name resolution)

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ DHCP uses TCP → ❌ Wrong
* ✔ DHCP lease can expire
* ✔ Static IP ≠ DHCP reservation
* ✔ DHCP client port = **68**

---

### 🔧 **Corrections / Improvements**

* Modern Linux uses **NetworkManager + DHCP**
* DHCP failover supported in enterprise setups

---

---

## 🧩 **3️⃣ Configuring a DNS Server** 🌐

### 🔹 **Concept Overview**

* **DNS (Domain Name System)** resolves:

  * Domain name → IP address
* Acts as the **Internet’s phonebook**

---

### 📘 **Key Definitions**

* **Forward Lookup:** Name → IP
* **Reverse Lookup:** IP → Name
* **Zone File:** Database of DNS records
* **FQDN:** Fully Qualified Domain Name

---

### 📚 **Main Content**

#### 🔸 **Common DNS Server in Linux**

* **BIND (Berkeley Internet Name Domain)**

#### 🔸 **Installation**

```bash
sudo apt install bind9
```

#### 🔸 **Key Files**

* `/etc/bind/named.conf`
* `/etc/bind/named.conf.local`
* `/var/lib/bind/`

#### 🔸 **DNS Records**

| Record | Purpose        |
| ------ | -------------- |
| A      | Name → IPv4    |
| AAAA   | Name → IPv6    |
| CNAME  | Alias          |
| MX     | Mail server    |
| NS     | Name server    |
| PTR    | Reverse lookup |

---

### 📌 **Important Facts for MCQs**

* DNS uses **UDP 53** (TCP for zone transfer)
* BIND is most popular Linux DNS server
* Reverse lookup uses **PTR record**

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ DNS assigns IP → ❌ DHCP does
* ✔ One domain can have multiple A records
* ✔ Cached DNS improves performance
* ✔ `/etc/resolv.conf` stores DNS client info

---
Just tell me 👍
