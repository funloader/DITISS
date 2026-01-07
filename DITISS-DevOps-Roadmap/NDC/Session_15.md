# **Session 15 – Snort IDS, IDS Architecture & IDS Bypassing (PG-DITISS)**

---

## 1. **Concept Overview**

Session 15 focuses on:

* **Testing Snort IDS** on **Windows & Linux**
* Understanding **IDS architecture**
* Recognizing **techniques used to bypass IDS**

Core idea:

> **IDS effectiveness depends on correct deployment, tuning, and resistance to evasion techniques**

---

## 2. **Key Definitions**

| Term             | Exam-Oriented Definition            |
| ---------------- | ----------------------------------- |
| Snort            | Open-source network-based IDS/IPS   |
| IDS Architecture | Structural design of IDS components |
| Signature        | Pattern used to detect attacks      |
| IDS Evasion      | Technique to avoid IDS detection    |

---

## 3. **Main Content (Organized as per Syllabus)**

---

## **A. Testing Snort in Windows & Linux**

---

### **Snort – Overview**

**Snort** is a:

* Open-source
* Network-based IDS (NIDS)
* Developed by **Martin Roesch**
* Uses **rule-based detection**

📌 *Snort can run as IDS, IPS, or packet sniffer*

---

### **Snort Operating Modes (High MCQ Value)**

| Mode               | Description                 |
| ------------------ | --------------------------- |
| Sniffer Mode       | Displays packets            |
| Packet Logger Mode | Logs packets                |
| IDS Mode           | Detects attacks using rules |
| IPS Mode           | Blocks traffic (inline)     |

---

### **Snort on Linux**

* Native support
* Commonly deployed on servers
* Uses command-line configuration
* Better performance & stability

---

### **Snort on Windows**

* Used mainly for:

  * Testing
  * Learning
* Requires WinPcap / Npcap
* Limited enterprise deployment

📌 *Linux is preferred for production Snort deployments*

---

### **Testing Snort (Exam-Oriented Steps)**

1. Install Snort
2. Configure rules
3. Start Snort in IDS mode
4. Generate traffic/attack
5. Verify alerts/logs

---

## **B. IDS Architecture**

---

### **IDS Architecture – Definition**

IDS architecture defines:

* How data is collected
* How analysis is performed
* How alerts are managed

---

### **Core Components of IDS Architecture**

| Component          | Function               |
| ------------------ | ---------------------- |
| Sensors            | Collect traffic/data   |
| Analysis Engine    | Detects intrusions     |
| Signature Database | Stores attack patterns |
| Alerting System    | Generates alerts       |
| Management Console | Central monitoring     |

📌 *Architecture can be centralized or distributed*

---

### **Centralized vs Distributed IDS**

| Feature     | Centralized | Distributed   |
| ----------- | ----------- | ------------- |
| Sensors     | Few         | Many          |
| Analysis    | Central     | Central/Local |
| Scalability | Limited     | High          |

---

## **C. Bypassing an IDS**

---

### **IDS Bypassing – Concept**

**IDS bypassing** refers to:

* Techniques attackers use
* To evade detection mechanisms

📌 *Bypassing exploits weaknesses in detection logic*

---

### **Common IDS Evasion Techniques (High MCQ Value)**

| Technique             | Description                   |
| --------------------- | ----------------------------- |
| Packet fragmentation  | Breaks attack payload         |
| Obfuscation           | Encodes payload               |
| Polymorphism          | Changes attack signature      |
| Timing attacks        | Slows traffic                 |
| Protocol manipulation | Exploits protocol ambiguities |
| Encryption            | Hides payload                 |

📌 *Signature-based IDS is most vulnerable to evasion*

---

### **Why IDS Can Be Bypassed**

* Outdated signatures
* Poor tuning
* Encrypted traffic
* High false positives → disabled rules

---

## 4. **Important Facts / Points for MCQs**

* Snort is rule-based IDS
* Snort supports IDS & IPS modes
* Linux preferred for Snort deployment
* IDS uses signatures for detection
* Encryption reduces IDS visibility
* Packet fragmentation bypasses detection

---

## 5. **Examples (Exam-Friendly)**

* Running Snort on Ubuntu → Linux IDS
* Viewing alerts → IDS mode
* Breaking payload into packets → IDS evasion
* Central dashboard → IDS manager
* Encrypted HTTPS traffic → Detection blind spot

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions**

* Snort ≠ Firewall
* IDS ≠ IPS
* Sniffer mode ≠ IDS mode
* Encryption ≠ IDS protection
* Evasion ≠ Exploit

---

