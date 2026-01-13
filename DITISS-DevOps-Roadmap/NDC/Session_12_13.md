
# **Session 12 & 13 – IDS Architecture, Sensors, DoS & Mitigation (PG-DITISS)**

---

## 1. **Concept Overview**

Session 12 & 13 focus on:

* **Recognizing attack symptoms**
* **Tiered IDS architecture**
* **Sensors and agents**
* **Denial of Service (DoS / DDoS)**
* **Deployment and management of IDS components**

Core idea:

> **Effective intrusion detection depends on correct architecture, sensor placement, and timely response**

---

## 2. **Key Definitions**

| Term                | Exam-Oriented Definition                  |
| ------------------- | ----------------------------------------- |
| Attack Symptoms     | Observable signs indicating an attack     |
| Tiered Architecture | Multi-layer IDS design                    |
| Sensor              | Component that collects security data     |
| Agent               | Software performing detection tasks       |
| IDS Manager         | Central control & analysis unit           |
| DoS                 | Attack that disrupts service availability |
| DDoS                | Distributed DoS using multiple sources    |

---

## 3. **Main Content (Organized as per Syllabus)**

---

## **A. Symptoms of Attacks**

### **Common Attack Symptoms (High MCQ Value)**

* Unusual network traffic
* Multiple failed login attempts
* Sudden performance degradation
* Unexpected system reboots
* Unauthorized file changes
* Abnormal CPU / memory usage
* Frequent service crashes

📌 *Symptoms indicate attack possibility, not confirmation*

---

## **B. Tiered Architecture**

---

### **Tiered IDS Architecture – Definition**

A **tiered architecture**:

* Divides IDS into multiple layers
* Improves scalability and manageability

---

### **Typical IDS Tiers**

| Tier            | Function                     |
| --------------- | ---------------------------- |
| Sensor Tier     | Data collection              |
| Analysis Tier   | Detection & correlation      |
| Management Tier | Control, reporting, response |

📌 *Tiered architecture reduces processing overhead*

---

## **C. Sensors – Network & Host Based**

---

### **1. Network-Based Sensors**

* Monitor network traffic
* Placed at:

  * Gateways
  * DMZ
  * Core switches

**Detects:**

* Network scans
* DoS attacks
* Protocol anomalies

---

### **2. Host-Based Sensors**

* Installed on hosts
* Monitor:

  * Logs
  * File integrity
  * System calls

**Detects:**

* Insider attacks
* Privilege escalation

📌 *Sensors collect data; analysis happens centrally*

---

## **D. Denial of Service (DoS)**

---

### **DoS – Definition**

A **DoS attack**:

* Aims to make services unavailable
* Exhausts system or network resources

---

### **Types of DoS Attacks**

| Type              | Description                 |
| ----------------- | --------------------------- |
| Flooding          | Excessive traffic           |
| Protocol attacks  | Exploit protocol weaknesses |
| Application-layer | Target specific services    |

---

### **DDoS**

* Multiple attacking systems
* Uses botnets
* Harder to mitigate

📌 *Availability is primary target*

---

## **E. DoS & DDoS Mitigation**

---

### **Mitigation Techniques**

* Rate limiting
* Traffic filtering
* Load balancing
* IDS/IPS detection
* Anycast routing
* Blackholing traffic

📌 *Mitigation focuses on availability restoration*

---

## **F. Sensor Deployment**

---

### **Best Practices for Sensor Deployment**

* Place at network choke points
* Deploy both NIDS & HIDS
* Avoid encrypted blind spots
* Ensure high availability

📌 *Incorrect placement reduces detection effectiveness*

---

## **G. Agents**

---

### **Agent – Definition**

An **IDS agent** is:

* Software component
* Performs monitoring & detection tasks
* Reports to IDS manager

---

### **Types of Agents**

* Network agents
* Host agents
* Log agents

---

## **H. Functions of IDS Agents**

---

### **Key Functions (MCQ-Oriented)**

* Data collection
* Event detection
* Local analysis
* Alert generation
* Log forwarding
* Policy enforcement

📌 *Agents operate under manager control*

---

## **I. IDS Manager**

---

### **IDS Manager – Definition**

An **IDS Manager**:

* Centralized management component
* Controls agents & sensors

---

### **Functions of IDS Manager**

* Policy management
* Alert correlation
* Event analysis
* Reporting
* Response coordination

📌 *Manager ≠ Sensor*

---

## 4. **Important Facts / Points for MCQs**

* Symptoms ≠ Proof of attack
* Tiered architecture improves scalability
* Sensors collect data
* Agents perform detection
* IDS manager controls system
* DoS targets availability

---

## 5. **Examples (Exam-Friendly)**

* Traffic spike → DoS symptom
* Core switch sensor → NIDS
* File integrity alert → Host sensor
* Botnet flooding → DDoS
* Central console → IDS manager

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions**

* Sensor ≠ Agent
* DoS ≠ DDoS
* Symptom ≠ Incident
* IDS manager ≠ Detection engine
* Network sensor ≠ Host sensor


---
