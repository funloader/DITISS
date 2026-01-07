# **Session 10 & 11 – Attacks, IDS/IPS Architecture & Threat Hunting (PG-DITISS)**

---

## 1. **Concept Overview**

Session 10 & 11 deepen intrusion concepts by covering:

* **Traditional vs Distributed attacks**
* **Intruder classification**
* **IDS & IPS types and categories**
* **Defence in Depth strategy**
* **IDS/IPS analysis & detection methodologies**
* **Principles of IDS**
* **Threat Hunting model**

Core idea:

> **Modern security relies on layered defense, intelligent detection, and proactive threat hunting**

---

## 2. **Key Definitions**

| Term                  | Exam-Oriented Definition              |
| --------------------- | ------------------------------------- |
| Traditional Attack    | Attack launched from a single source  |
| Distributed Attack    | Attack launched from multiple sources |
| Intruder              | Entity attempting unauthorized access |
| Defence in Depth      | Multiple layers of security controls  |
| Detection Methodology | Technique used to identify attacks    |
| Threat Hunting        | Proactive search for hidden threats   |

---

## 3. **Main Content (Organized as per Syllabus)**

---

## **A. Attacks – Traditional vs Distributed**

---

### **1. Traditional Attacks**

**Characteristics:**

* Single attacker or source
* Easier to trace
* Limited impact

**Examples:**

* Single-source DoS
* Password guessing

---

### **2. Distributed Attacks**

**Characteristics:**

* Multiple compromised systems
* Harder to trace
* High impact

**Examples:**

* DDoS attacks
* Botnet-based attacks

📌 *Most modern attacks are distributed*

---

## **B. Intruder Types**

---

### **Classification of Intruders (MCQ Favorite)**

| Intruder Type    | Description                                     |
| ---------------- | ----------------------------------------------- |
| Masquerader      | External attacker pretending as legitimate user |
| Misfeasor        | Insider misusing privileges                     |
| Clandestine user | Gains supervisory control and hides activity    |

📌 *Insiders are the most dangerous*

---

## **C. Types of IDS**

---

### **1. Network-Based IDS (NIDS)**

* Monitors network traffic
* Detects network-level attacks

---

### **2. Host-Based IDS (HIDS)**

* Installed on hosts
* Monitors logs, file integrity

---

### **3. Hybrid IDS**

* Combines NIDS + HIDS

📌 *Hybrid IDS offers better visibility*

---

## **D. IPS Categories**

---

### **IPS Classification (Exam-Oriented)**

| IPS Type                        | Description                 |
| ------------------------------- | --------------------------- |
| Network-based IPS (NIPS)        | Protects network segments   |
| Host-based IPS (HIPS)           | Protects individual systems |
| Wireless IPS (WIPS)             | Protects wireless networks  |
| Network Behavior Analysis (NBA) | Detects anomalies           |

📌 *IPS operates inline*

---

## **E. Defence in Depth**

---

### **Defence in Depth – Definition**

A **layered security approach** where:

* Multiple controls protect assets
* Failure of one layer does not compromise system

---

### **Security Layers**

* Physical security
* Network security
* Host security
* Application security
* Data security
* Policy & awareness

📌 *Defence in depth reduces single point of failure*

---

## **F. IDS and IPS Analysis Scheme**

---

### **IDS/IPS Analysis Workflow**

1. Data collection
2. Preprocessing
3. Detection analysis
4. Alert generation
5. Response action (IPS)

📌 *IDS generates alerts; IPS enforces action*

---

## **G. Detection Methodologies**

---

### **1. Signature-Based Detection**

* Matches known attack patterns
* Low false positives
* Cannot detect zero-day attacks

---

### **2. Anomaly-Based Detection**

* Detects deviation from normal behavior
* Can detect zero-day attacks
* High false positives

---

### **3. Specification-Based Detection**

* Uses predefined behavior rules
* Hybrid approach

📌 *Most systems use hybrid detection*

---

## **H. Principles of IDS**

---

### **Core Principles (MCQ-Important)**

* Continuous monitoring
* Accuracy
* Timeliness
* Scalability
* Low false positives
* Minimal performance impact

📌 *IDS should not affect normal operations*

---

## **I. Threat Hunting Model**

---

### **Threat Hunting – Definition**

Threat hunting is:

* **Proactive security approach**
* Identifies threats not detected by tools

---

### **Threat Hunting Cycle**

1. Hypothesis creation
2. Data collection
3. Investigation
4. Detection & confirmation
5. Remediation
6. Feedback & improvement

📌 *Threat hunting is human-driven*

---

### **Threat Hunting Inputs**

* Logs
* Network traffic
* Endpoint telemetry
* Threat intelligence

---

## 4. **Important Facts / Points for MCQs**

* Distributed attacks use botnets
* Masquerader = external attacker
* Hybrid IDS = NIDS + HIDS
* IPS works inline
* Defence in depth uses layered controls
* Anomaly detection finds zero-days

---

## 5. **Examples (Exam-Friendly)**

* Botnet attack → Distributed attack
* Insider misuse → Misfeasor
* Wireless attack detection → WIPS
* Multiple security layers → Defence in depth
* Proactive investigation → Threat hunting

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions**

* Traditional ≠ Distributed attack
* IDS ≠ IPS
* Signature ≠ Anomaly detection
* Defence in depth ≠ Multiple firewalls only
* Threat hunting ≠ Automated detection

---
