# **Session 2 – Risk Management, Firewall & DMZ (PG-DITISS)**

---

## 1. **Concept Overview**

Session 2 focuses on:

* **Managing security risks**
* **Reducing exposure**
* **Using firewalls and DMZs as countermeasures**
* Understanding **how firewalls are implemented**

Core idea:

> **Risk cannot be eliminated, only reduced to an acceptable level**

---

## 2. **Key Definitions**

| Term            | Exam-Oriented Definition                                    |
| --------------- | ----------------------------------------------------------- |
| Risk Management | Process of identifying, assessing, and controlling risks    |
| Risk Exposure   | Potential loss due to a security incident                   |
| Countermeasure  | Control used to reduce risk                                 |
| Firewall        | Device/software that filters network traffic based on rules |
| DMZ             | Isolated network segment for public-facing services         |

---

## 3. **Main Content (Organized from Notes)**

---

## **A. Risk Management, Exposure & Countermeasure**

### **1. Risk Management**

**Definition:**
A structured process to **identify, analyze, mitigate, and monitor risks** affecting information assets.

### **Steps in Risk Management**

1. **Risk Identification**

   * Identify threats & vulnerabilities
2. **Risk Assessment**

   * Likelihood × Impact
3. **Risk Mitigation**

   * Apply controls / countermeasures
4. **Risk Monitoring**

   * Continuous review

📌 *Risk management is a continuous cycle*

---

### **2. Risk Exposure**

**Risk Exposure** refers to:

* Expected **loss or damage** if a threat occurs

**Examples:**

* Financial loss
* Data breach
* Reputation damage
* Legal penalties

📌 *Higher exposure = higher business impact*

---

### **3. Countermeasures**

**Countermeasures** are controls used to:

* Reduce probability of attack
* Reduce impact of attack

**Examples (from notes):**

* Firewalls
* Antivirus software
* IDS / IPS
* Access control
* Employee security awareness

---

## **B. Firewall**

### **Firewall – Definition**

A **firewall** is a **hardware or software security device** that:

* Monitors **incoming and outgoing traffic**
* Allows or blocks traffic based on **security rules**

📌 *First line of defense in network security*

---

### **Firewall Characteristics**

* Can be **hardware, software, or hybrid**
* Separates:

  * Trusted internal network
  * Untrusted external network (Internet)
* Enforces **security policy**

---

### **Types of Firewalls (Exam-Relevant Names)**

* Packet Filter Firewall
* Stateful Inspection Firewall
* Proxy Server Firewall
* Application-Level Firewall
* Screened Host Firewall
* Screened Subnet Firewall
* Hybrid Firewall

⚠️ *PG-DITISS MCQs often ask firewall type vs OSI layer*

---

## **C. De-Militarized Zone (DMZ)**

### **DMZ – Definition**

A **DMZ (Demilitarized Zone)** is a **separate network segment** placed:

* Between **Internet and Internal Network**
* Hosts **public-facing services**

---

### **Purpose of DMZ**

* Adds **extra security layer**
* Limits internal network exposure
* Contains compromise impact

---

### **Services Typically Placed in DMZ**

* Web servers
* Mail servers
* DNS servers
* FTP servers

---

### **DMZ Characteristics**

| Feature        | Description                           |
| -------------- | ------------------------------------- |
| Segregation    | Logical/physical isolation            |
| Limited Access | Controlled access to internal network |
| Dual Firewalls | Internal + External firewall          |
| Monitoring     | Logs, IDS, vulnerability scans        |

📌 *DMZ ≠ Trusted network*

---

## **D. Two Methods of Implementing Firewall**

---

### **1. Network-Based Firewall**

**Definition:**

* Deployed at **network boundary**
* Protects entire network

**Features:**

* Centralized control
* Hardware or software
* Blocks network-level attacks (DoS, scans)

**Advantages:**

* One firewall protects many systems
* Easier management

---

### **2. Host-Based Firewall**

**Definition:**

* Installed on **individual systems**
* Protects specific host

**Features:**

* OS-based or software-based
* Granular control per device

**Advantages:**

* Device-specific security
* Protects even inside network

📌 *Best practice → Use both together*

---

## 4. **Important Facts / Points for MCQs**

* Risk Exposure depends on **likelihood + impact**
* Countermeasures reduce **risk, not threats**
* Firewall is **preventive control**
* DMZ hosts **public services only**
* Network firewall ≠ Host firewall
* Firewalls enforce **security policy**

---

## 5. **Examples (If Applicable)**

* Public web server placed in DMZ → **Correct architecture**
* Antivirus software → **Countermeasure**
* Firewall blocking port 80 → **Risk mitigation**
* Database server in DMZ → ❌ **Security violation**

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions:**

* Risk ≠ Threat
* Countermeasure ≠ Risk elimination
* DMZ ≠ Internal network
* Firewall ≠ IDS
* Host firewall ≠ Network firewall

---

