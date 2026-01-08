# 📘 Session 14: NAT, IPv6 & WAN Technologies
---

## 🌐 **1. NAT (Network Address Translation)**

### 📌 **Concept Overview**

* **NAT** allows **private (internal) IP addresses** to communicate with **public (external) networks** by translating IP addresses.
* Commonly implemented on **routers / firewalls / gateways**.
* Widely used due to **IPv4 address exhaustion**.

---

### 📖 **Key Definitions**

* **Private IP Address**: Non-routable IP (e.g., 10.x.x.x, 172.16–31.x.x, 192.168.x.x)
* **Public IP Address**: Globally routable IP assigned by ISP
* **Translation Table**: Mapping maintained by NAT device
* **PAT (Port Address Translation)**: Uses port numbers along with IP

---

### 🧱 **Types of NAT**

| Type                   | Description                                              |
| ---------------------- | -------------------------------------------------------- |
| **Static NAT**         | One private IP ↔ One public IP (fixed mapping)           |
| **Dynamic NAT**        | Private IP mapped to any IP from public pool             |
| **PAT / NAT Overload** | Multiple private IPs share **one public IP** using ports |

---

### ⭐ **Advantages of NAT**

* Conserves IPv4 addresses
* Improves internal network security
* Hides internal IP structure

### ⚠️ **Disadvantages of NAT**

* Breaks **end-to-end connectivity**
* Issues with some protocols (VoIP, FTP active mode)
* Adds processing overhead

---

### 🧠 **Important Facts for MCQs**

* NAT works at **Network Layer (Layer 3)**
* PAT uses **Layer 4 (Port numbers)** additionally
* NAT is **not a security mechanism**, but provides obscurity
* Private IPs are defined in **RFC 1918**

---

### 🧪 **Examples**

* Home Wi-Fi router translating 192.168.1.x → single public IP
* Corporate LAN accessing internet via firewall NAT

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ NAT ≠ Firewall
* ❌ NAT does NOT encrypt traffic
* ✔ PAT = NAT Overload
* ✔ NAT mainly exists due to **IPv4 limitation**

---

### 🔧 **Corrections / Improvements / Suggested Substitutions**

* If notes imply NAT = security → ❗Correct: **NAT only hides IPs**
* Use term **PAT** instead of “many-to-one NAT” for accuracy

---

---

## 🌍 **2. IPv6 (Internet Protocol Version 6)**

### 📌 **Concept Overview**

* **IPv6** is the successor of IPv4, designed to solve **address exhaustion**.
* Uses **128-bit addressing**.

---

### 📖 **Key Definitions**

* **IPv6 Address Length**: 128 bits
* **Hexadecimal Representation** (base 16)
* **No NAT required** in IPv6

---

### 🧱 **IPv6 Address Format**

* Example:
  `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
* Leading zeros can be omitted
* Consecutive zeros replaced with `::` (once only)

---

### 🧩 **Types of IPv6 Addresses**

| Type            | Purpose                   |
| --------------- | ------------------------- |
| **Unicast**     | One-to-one communication  |
| **Multicast**   | One-to-many               |
| **Anycast**     | One-to-nearest            |
| ❌ **Broadcast** | **Not supported in IPv6** |

---

### ⭐ **Key Features of IPv6**

* Huge address space (2¹²⁸)
* No NAT required
* Built-in **IPSec support**
* Simplified header
* Auto-configuration (SLAAC)

---

### 🧠 **Important Facts for MCQs**

* IPv6 replaces **ARP with NDP**
* No broadcast → uses multicast
* Header size is **fixed (40 bytes)**
* IPv6 uses **ICMPv6**

---

### 🧪 **Examples**

* Loopback: `::1`
* Link-local: `fe80::/10`
* Global unicast: `2000::/3`

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ IPv6 does NOT use NAT
* ❌ No broadcast in IPv6
* ✔ IPv6 uses hexadecimal
* ✔ IPv6 header is simpler than IPv4

---

### 🔧 **Corrections / Improvements / Suggested Substitutions**

* Replace “IPv6 is slower” → ❗Incorrect
* Correct term: **NDP instead of ARP**

---

---

## 🌐 **3. WAN Technologies**

### 📌 **Concept Overview**

* **WAN (Wide Area Network)** connects networks over **large geographical areas**.
* Uses **service provider infrastructure**.

---

### 📖 **Key Definitions**

* **WAN**: Network spanning cities/countries
* **ISP**: Internet Service Provider
* **Bandwidth**: Data transfer capacity

---

### 🧱 **Common WAN Technologies**

| Technology      | Description                    |
| --------------- | ------------------------------ |
| **Leased Line** | Dedicated point-to-point link  |
| **ISDN**        | Digital telephone-based WAN    |
| **MPLS**        | Label-based high-speed routing |
| **Frame Relay** | Packet-switched WAN (legacy)   |
| **ATM**         | Cell-based (53 bytes)          |
| **DSL**         | Uses telephone lines           |
| **VSAT**        | Satellite-based WAN            |

---

### ⭐ **Advantages of WAN**

* Long-distance connectivity
* Centralized data access
* Scalable enterprise networks

### ⚠️ **Disadvantages**

* Expensive
* Higher latency
* ISP dependency

---

### 🧠 **Important Facts for MCQs**

* WAN uses **Layer 2 & Layer 3 technologies**
* MPLS is **protocol-independent**
* ATM cell size = **53 bytes**
* Leased line = **always-on connection**

---

### 🧪 **Examples**

* Bank branches connected via MPLS
* Corporate HQ ↔ Branch via leased line
* Remote areas using VSAT

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ WAN ≠ Internet
* ✔ LAN is faster than WAN
* ❌ Frame Relay is obsolete but still asked in exams
* ✔ MPLS ≠ protocol, it’s a switching technique

---
