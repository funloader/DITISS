# SESSION 2 – COMPUTER FORENSICS OPERATIONS & INCIDENT HANDLING

---

## **1. Computer Forensics Involves**

Computer forensics is a **systematic and legally defensible process** consisting of the following core activities:

1. **Preservation**
2. **Identification**
3. **Extraction**
4. **Documentation**
5. **Interpretation**

📌 **MCQ Trap**:
These are **operational activities**, NOT the six-stage investigation lifecycle.

---

## **2. Preservation**

### **Purpose**

* Maintain **original state** of digital evidence
* Prevent **alteration, damage, or loss**

### **Key Actions**

* Create **forensic image / duplicate**
* Use write-blockers
* Protect from electromagnetic damage
* Secure storage with access control

📌 **MCQ Trap**:

* Analysis is **never performed on original evidence**

---

## **3. Identification**

### **Definition**

* Identifying **potential sources of digital evidence**

### **Includes**

* Devices (PCs, mobiles, storage)
* Systems & networks
* Files, logs, artifacts relevant to case

📌 **MCQ Trap**:

* Identification ≠ Collection

---

## **4. Extraction**

### **Purpose**

* Extract relevant data **without modifying original evidence**

### **Techniques**

* Recovery of deleted / hidden files
* Metadata extraction
* File system analysis
* Accessing encrypted data (if possible)

📌 **MCQ Trap**:

* Extraction is performed on **forensic copy**, not live original (unless live forensics).

---

## **5. Documentation**

### **Importance**

* Ensures **auditability** and **legal admissibility**

### **What is Documented**

* Steps performed
* Tools used
* Timestamps
* Observations & findings

📌 **MCQ Trap**:

* Poor documentation = evidence rejected in court

---

## **6. Interpretation**

### **Purpose**

* Convert extracted data into **meaningful conclusions**

### **Includes**

* Event reconstruction
* Pattern identification
* Correlation of evidence
* Drawing conclusions

📌 **MCQ Trap**:

* Interpretation is **analytical**, not mechanical

---

## **7. Goals of Forensics Analysis**

1. **Identification & Attribution**

   * Link actions to individuals or systems
2. **Evidence Collection & Preservation**

   * Maintain integrity & admissibility
3. **Incident Reconstruction**

   * Timeline & sequence of events
4. **Data Recovery**

   * Deleted, lost, damaged data
5. **Analysis & Interpretation**

   * Patterns, anomalies, correlations
6. **Reporting & Documentation**

   * Clear, court-ready reports
7. **Expert Testimony**

   * Explain findings in legal proceedings

📌 **MCQ Trap**:

* Forensics goal ≠ system repair

---

## **8. Types of Cyber Forensics Techniques**

### **1. Disk Imaging**

* Bit-by-bit copy
* Preserves original evidence

### **2. File Carving**

* Recover deleted / fragmented files
* Based on file signatures

### **3. Network Traffic Analysis**

* Analyze packets, flows, logs
* Detect intrusions & data exfiltration

### **4. Memory Forensics**

* Analyze volatile memory (RAM)
* Identify running processes, keys, malware

### **5. Email Forensics**

* Headers, timestamps, attachments
* Trace origin and communication

### **6. Mobile Device Forensics**

* Calls, SMS, app data, media files

### **7. Malware Analysis**

* Behavior, origin, impact
* Reverse engineering, sandboxing

### **8. Log File Analysis**

* System, application, security logs
* Detect anomalies & reconstruct events

📌 **MCQ Trap**:

* RAM evidence is **volatile**

---

## **9. Cyber Forensics Procedures**

### **1. Planning & Preparation**

* Define scope & objectives
* Legal authorization
* Tool & resource planning

### **2. Evidence Identification & Preservation**

* Secure scene
* Create forensic images

### **3. Evidence Collection**

* Disk, memory, logs, network data
* Maintain chain of custody

### **4. Evidence Analysis**

* File, log, network, metadata analysis

### **5. Evidence Reconstruction**

* Build timeline
* Cause-effect relationships

### **6. Reporting & Documentation**

* Comprehensive, clear reports

### **7. Presentation & Expert Testimony**

* Court presentation & explanation

📌 **MCQ Trap**:

* Procedures must follow **forensic guidelines**

---

## **10. Preparation (Before Incident)**

Preparation is **pre-incident readiness**.

### **What to Do Before the Incident**

* Cybersecurity policy
* Risk & vulnerability assessments
* Firewalls, IDS/IPS, antivirus
* User awareness & training

📌 **MCQ Trap**:

* Preparation ≠ Detection

---

## **11. Incident Response Plan (IRP)**

### **Purpose**

* Step-by-step incident handling guide

### **Includes**

* Roles & responsibilities
* Incident classification
* Evidence preservation
* Communication & escalation
* Legal considerations

📌 **MCQ Trap**:

* IRP is **pre-defined**, not created after incident

---

## **12. Incident Response Team (IRT)**

### **Composition**

* IT
* Forensics
* Legal
* HR
* Management
* Communications

### **Key Features**

* Defined roles
* Clear communication
* Central coordination

📌 **MCQ Trap**:

* Incident response is **multi-disciplinary**

---

## **13. Detecting Incidents**

### **Techniques**

1. Log Analysis
2. Network Traffic Analysis
3. IDS / IPS
4. Endpoint Detection & Response (EDR)
5. Digital Forensic Analysis
6. Threat Intelligence
7. User Behavior Analytics (UBA)

📌 **MCQ Trap**:

* Detection ≠ Investigation

---

## **14. Chain of Custody**

### **Definition**

* Documentation of **custody, control, transfer** of evidence

### **Key Elements**

* Documentation
* Sealing & packaging
* Labeling
* Transfer records
* Secure storage
* Access logs
* Evidence preservation

### **Purpose**

* Ensure **authenticity**
* Maintain **admissibility in court**

📌 **MCQ Trap**:

* Broken chain of custody = evidence invalid

---

# **EXAM QUICK REVISION (One-Look Points)**

* Preservation = integrity
* Identification ≠ extraction
* Documentation is **mandatory**
* RAM evidence = volatile
* Incident response starts **before incident**
* Chain of custody is **continuous**

---

## **Corrections / Improvements / Suggested Substitutions**

1. **Avoid mixing**:

   * “Process of forensics” vs “Forensics involves” (asked separately in exams)
2. **Remember sequences**:

   * Preservation → Identification → Extraction → Documentation → Interpretation
3. **Do not confuse**:

   * Incident detection with incident response
4. **Chain of custody**:

   * Documentation is more important than tools
5. **Preparation questions**:

   * Mostly asked as **pre-incident MCQs**

---

