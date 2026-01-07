# **Session 9 – IDS, IPS, Attacks & Security Events (PG-DITISS)**

---

## 1. **Concept Overview**

Session 9 introduces **Intrusion Detection and Prevention Systems** and focuses on:

* Detecting and preventing attacks
* Understanding **types of attacks**
* Identifying **security events**
* Linking attacks to **vulnerabilities (design, implementation, configuration)**

Core idea:

> **IDS detects attacks; IPS detects and blocks attacks**

---

## 2. **Key Definitions**

| Term           | Exam-Oriented Definition                  |
| -------------- | ----------------------------------------- |
| IDS            | System that detects malicious activity    |
| IPS            | System that detects and prevents attacks  |
| Intrusion      | Unauthorized or malicious activity        |
| Security Event | Observable occurrence related to security |
| Vulnerability  | Weakness that can be exploited            |

---

## 3. **Main Content (Organized as per Syllabus)**

---

## **A. Introduction to IDS and IPS**

### **Why IDS / IPS are Needed**

* Firewalls cannot detect:

  * Application-layer attacks
  * Insider threats
* IDS/IPS provide:

  * Visibility into attacks
  * Real-time monitoring
  * Attack response

📌 *IDS/IPS complement firewalls, not replace them*

---

## **B. IDS / IPS**

---

### **IDS (Intrusion Detection System)**

**Definition:**
An **IDS**:

* Monitors network/system activity
* Detects suspicious behavior
* Generates alerts

**Key Point:**
➡ IDS is a **passive control**

---

### **IPS (Intrusion Prevention System)**

**Definition:**
An **IPS**:

* Monitors traffic inline
* Detects and **blocks attacks**
* Takes automatic action

**Key Point:**
➡ IPS is an **active control**

---

### **IDS vs IPS (High MCQ Value)**

| Feature      | IDS             | IPS              |
| ------------ | --------------- | ---------------- |
| Action       | Detect & alert  | Detect & block   |
| Deployment   | Out-of-band     | Inline           |
| Traffic flow | Does not affect | Can drop packets |
| Control type | Detective       | Preventive       |

📌 *IPS can impact network performance*

---

## **C. Types of Attacks**

### **1. Network-Based Attacks**

* DoS / DDoS
* Port scanning
* Spoofing
* Man-in-the-middle

---

### **2. Host-Based Attacks**

* Malware
* Privilege escalation
* Unauthorized access

---

### **3. Application-Level Attacks**

* SQL Injection
* Cross-Site Scripting (XSS)
* Buffer overflow

---

### **4. Insider Attacks**

* Data theft
* Misuse of privileges

📌 *Most attacks exploit known vulnerabilities*

---

## **D. IDS (Detailed)**

---

### **Types of IDS (MCQ Favorite)**

#### **1. Network-Based IDS (NIDS)**

* Monitors network traffic
* Placed at strategic network points

---

#### **2. Host-Based IDS (HIDS)**

* Installed on individual hosts
* Monitors:

  * Logs
  * File integrity
  * System calls

---

### **IDS Detection Techniques**

| Technique       | Description                   |
| --------------- | ----------------------------- |
| Signature-based | Matches known attack patterns |
| Anomaly-based   | Detects deviation from normal |
| Heuristic-based | Rule/behavior-based           |

📌 *Signature-based cannot detect zero-day attacks*

---

## **E. Security Events**

---

### **Security Event – Definition**

A **security event** is:

* Any observable occurrence
* That may affect security

---

### **Examples of Security Events**

* Multiple failed login attempts
* Firewall rule violation
* Malware detection
* Unusual traffic spike

📌 *Not all events are incidents*

---

### **Event → Incident Flow**

| Term     | Meaning                   |
| -------- | ------------------------- |
| Event    | Logged occurrence         |
| Incident | Confirmed security breach |

---

## **F. Vulnerability: Design / Implementation**

---

### **Vulnerability – Definition**

A **vulnerability** is:

* Weakness in system that can be exploited

---

### **Types of Vulnerabilities**

#### **1. Design Vulnerability**

* Poor architecture
* Missing security controls
* Example: No authentication

---

#### **2. Implementation Vulnerability**

* Coding errors
* Buffer overflow
* Logic flaws

---

#### **3. Configuration Vulnerability** *(Implied & Exam-Relevant)*

* Weak passwords
* Open ports
* Default settings

📌 *Most real-world attacks exploit configuration flaws*

---

## 4. **Important Facts / Points for MCQs**

* IDS is detective control
* IPS is preventive control
* NIDS monitors traffic
* HIDS monitors hosts
* Signature-based IDS detects known attacks
* Vulnerability ≠ Threat

---

## 5. **Examples (Exam-Friendly)**

* SQL injection → Application attack
* Port scan detection → NIDS
* File integrity alert → HIDS
* Failed login attempts → Security event
* Buffer overflow → Implementation vulnerability

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions**

* IDS ≠ IPS
* Event ≠ Incident
* Vulnerability ≠ Attack
* NIDS ≠ Firewall
* Signature-based ≠ Anomaly-based

---

