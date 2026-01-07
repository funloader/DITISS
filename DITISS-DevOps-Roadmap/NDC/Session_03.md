# **Session 3 – Firewalls & Linux iptables (PG-DITISS)**

---

## 1. **Concept Overview**

Session 3 focuses on:

* **Firewall filtering techniques**
* **Host-based vs network-based protection**
* **Stateful vs stateless inspection**
* **Next Generation Firewall (NGFW) application control**
* **iptables as Linux firewall implementation**

Core idea:

> **Firewalls evolve from packet-based filtering to application-aware control**

---

## 2. **Key Definitions**

| Term                   | Definition (Exam-Oriented)                        |
| ---------------------- | ------------------------------------------------- |
| Packet Filtering       | Filtering packets based on IP, port, protocol     |
| Screened Host Firewall | Host-based firewall protecting individual systems |
| Stateful Inspection    | Firewall tracks connection state                  |
| NGFW                   | Firewall with application & user awareness        |
| iptables               | Linux firewall tool using rule-based filtering    |

---

## 3. **Main Content (Organized from Notes)**

---

## **A. Packet Filtering Firewall**

### **Definition**

A **packet filter firewall**:

* Examines **each packet individually**
* Uses **predefined rules (ACLs)**
* Works at **Network Layer (OSI Layer 3)**

---

### **Key Characteristics**

* **Stateless filtering**
* Checks:

  * Source IP
  * Destination IP
  * Port numbers
  * Protocol (TCP/UDP/ICMP)
* **Does NOT inspect packet payload**

---

### **Advantages**

* High performance
* Low processing overhead
* Transparent to users

---

### **Limitations**

* No application awareness
* Cannot track session state
* Weak against spoofing

---

📌 *Packet filtering = simplest firewall technique*

---

## **B. Screened Host Firewall**

### **Definition**

A **screened host firewall**:

* Installed on **individual hosts**
* Also called **host-based / personal firewall**
* Protects a **single system**

---

### **Key Features**

* Application-level filtering
* Stateful inspection
* User authentication
* Logging & alerting
* Integrates with antivirus / IDS

---

### **Use Case**

* Servers
* End-user systems
* Laptops

📌 *Provides granular protection per host*

---

## **C. Stateful Inspection Firewall**

### **Definition**

A **stateful inspection firewall**:

* Tracks **state of network connections**
* Filters packets based on **connection context**

---

### **Key Features**

* Maintains **state table**
* Allows packets only if part of:

  * NEW
  * ESTABLISHED
  * RELATED connections
* More secure than packet filtering

---

### **Advantages**

* Prevents spoofed packets
* Better traffic validation
* Application-level awareness

---

### **Comparison**

| Packet Filter | Stateful Firewall |
| ------------- | ----------------- |
| Stateless     | Stateful          |
| Fast          | Slightly slower   |
| Low security  | Higher security   |

---

📌 *Stateful firewalls are dynamic packet filters*

---

## **D. Next Generation Firewall (NGFW) – Application Controls**

### **NGFW Definition**

A **Next-Generation Firewall** goes beyond:

* Packet filtering
* Stateful inspection

And adds **application-level control**

---

### **NGFW Application Controls**

1. **Application Visibility**

   * Detects apps (even encrypted)
2. **Application Identification**

   * Identifies apps regardless of port
3. **Application Control**

   * Allow / block specific apps
4. **User-Based Control**

   * Policies based on user/role

---

### **Benefits**

* Prevents data leakage
* Controls social media & P2P
* Improves compliance

📌 *NGFW works at Layer 7 (Application Layer)*

---

## **E. iptables – Linux Firewall**

---

### **Definition**

**iptables** is a:

* Command-line firewall tool
* Used in Linux OS
* Implements **stateful packet filtering**

---

### **Working Principle**

* Inspects each packet
* Matches against **rules**
* Applies **targets**

---

### **iptables Tables (MCQ Favorite)**

| Table  | Purpose                            |
| ------ | ---------------------------------- |
| filter | Packet filtering (default)         |
| nat    | Network Address Translation        |
| mangle | Packet modification                |
| raw    | Exempt packets from state tracking |

---

### **iptables Chains**

| Chain   | Description                  |
| ------- | ---------------------------- |
| INPUT   | Incoming traffic to host     |
| OUTPUT  | Outgoing traffic from host   |
| FORWARD | Traffic passing through host |

---

### **iptables Targets**

| Target      | Action               |
| ----------- | -------------------- |
| ACCEPT      | Allow packet         |
| DROP        | Silently discard     |
| REJECT      | Drop + notify sender |
| LOG         | Log packet           |
| SNAT / DNAT | NAT operations       |

---

### **Common Commands (Exam-Oriented)**

* List rules:
  `iptables -L -n -v`
* Flush rules:
  `iptables -F`
* Block IP:
  `iptables -A INPUT -s IP -j DROP`
* Block port:
  `iptables -A INPUT -p tcp --dport 80 -j DROP`

📌 *iptables is stateful by default*

---

## 4. **Important Facts / Points for MCQs**

* Packet filtering = Stateless
* Stateful firewall tracks sessions
* NGFW identifies applications regardless of port
* iptables default table → **filter**
* INPUT chain → traffic to local system
* DROP vs REJECT → Silent vs Response

---

## 5. **Examples (If Applicable)**

* Blocking port 80 → Packet filtering
* Tracking TCP session → Stateful inspection
* Blocking Facebook app → NGFW
* Linux firewall configuration → iptables

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions**

* Packet filter ≠ Stateful firewall
* NGFW ≠ Traditional firewall
* iptables ≠ GUI firewall
* DROP ≠ REJECT
* Chain ≠ Table

---
