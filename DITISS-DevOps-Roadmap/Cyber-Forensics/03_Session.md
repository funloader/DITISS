# SESSION 3 – EVIDENCE HANDLING, RESPONSE & INVESTIGATION IN CYBER FORENSICS

---

## **1. Evidence Checkout Log**

### **Concept Overview**

* A formal record that tracks **movement, access, and handling** of digital evidence.

### **Key Contents**

* Evidence ID / description
* Date & time of checkout / return
* Purpose of access
* Name & signature of person handling evidence

### **Importance**

* Part of **Chain of Custody**
* Ensures **accountability & traceability**

📌 **MCQ Trap**

* Checkout log ≠ chain of custody (it is a **component** of it)

---

## **2. Handling Evidence**

### **Key Principles**

* Evidence must be:

  * **Preserved**
  * **Protected**
  * **Documented**

### **Best Practices**

* Use **write-blockers**
* Avoid booting suspect systems unnecessarily
* Store in secure, access-controlled environment
* Maintain hashes and logs

📌 **MCQ Trap**

* Mishandling can cause **evidence contamination**

---

## **3. First Response**

### **Definition**

* Immediate actions taken **after detection of an incident**

### **Objectives**

* Prevent further damage
* Preserve evidence
* Maintain system stability

### **Key Actions**

* Secure the scene
* Isolate affected systems
* Document system state
* Decide live vs dead analysis

📌 **MCQ Trap**

* First response ≠ forensic analysis

---

## **4. Formulate & Execute Response Strategy**

### **Formulation Includes**

* Incident severity assessment
* Scope identification
* Legal & regulatory considerations
* Resource allocation

### **Execution Includes**

* Containment
* Evidence acquisition
* Investigation initiation
* Communication with stakeholders

📌 **MCQ Trap**

* Response strategy must align with **incident response plan**

---

## **5. Forensic Duplication**

### **Definition**

* Creation of an **exact bit-by-bit copy** of digital evidence

### **Key Characteristics**

* Copies:

  * Visible files
  * Deleted files
  * Hidden data
  * File system metadata
  * Timestamps

### **Key Steps**

1. Bit-by-bit copying
2. Write-blocking
3. Hash verification
4. Documentation
5. Secure storage

📌 **MCQ Trap**

* File copy ≠ forensic duplication

---

## **6. Authenticate the Evidence**

### **Purpose**

* Prove **integrity, authenticity & admissibility**

### **Authentication Methods**

1. **Hash Values**

   * MD5, SHA-1, SHA-256
2. **Digital Signatures**
3. **Metadata Analysis**
4. **Chain of Custody Review**
5. **Forensic Tool Verification**
6. **Expert Witness Testimony**
7. **Audit Trails & Documentation**

📌 **MCQ Trap**

* Hash mismatch = evidence tampered

---

## **7. Investigation**

### **Definition**

* Systematic process to **collect, analyze, interpret** digital evidence

### **Key Steps**

1. Incident response & preparation
2. Evidence identification & collection
3. Forensic imaging
4. Data recovery & reconstruction
5. Timeline analysis
6. Malware analysis
7. Network forensics
8. Interpretation & reporting
9. Legal compliance
10. Expert testimony

📌 **MCQ Trap**

* Investigation is both **technical & legal**

---

## **8. Common Mistakes in Cyber Forensics**

### **Major Mistakes**

1. Poor documentation
2. Mishandling evidence
3. Lack of expertise
4. Ignoring volatile data
5. Insecure investigation environment
6. Single-source reliance
7. Legal & ethical violations
8. Lack of collaboration
9. Inadequate analysis
10. No continuous learning

📌 **MCQ Trap**

* Ignoring RAM = loss of volatile evidence

---

## **9. Detection**

### **Definition**

* Identifying **signs or indicators of cyber incidents**

### **Detection Techniques**

1. IDS (Signature-based & Behavior-based)
2. Log analysis
3. Network monitoring
4. Endpoint Detection & Response (EDR)
5. Threat intelligence
6. SIEM
7. Anomaly detection
8. User Behavior Analytics (UBA)
9. Honeypots / Honeynets
10. Incident reporting & monitoring

📌 **MCQ Trap**

* Detection precedes investigation

---

## **Important Facts / Points for MCQs**

* Evidence checkout log = tracking access
* Write-blocking prevents modification
* Forensic copy must be **bit-by-bit**
* Authentication relies heavily on **hash values**
* Investigation must follow legal standards
* Detection ≠ response ≠ investigation

---

## **MCQ Pointers / Exam Traps**

* File copy vs forensic image
* Chain of custody vs evidence log
* Detection vs first response
* Authentication vs authorization
* Preservation vs analysis
* Hashing vs encryption

---

## **Corrections / Improvements / Suggested Substitutions**

1. **MD5 usage**

   * Use **SHA-256** for integrity verification (MD5 weak due to collisions)
2. **Terminology**

   * Use *“forensic duplication”* instead of *backup*
3. **Authentication**

   * Hash verification must be done **before & after analysis**
4. **Detection**

   * Honeypots are **detection tools**, not prevention
5. **Common Mistakes**

   * Volatile data loss is a **frequent exam question**


Just tell me 👍
