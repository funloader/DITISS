# SESSION 4 – INITIAL ASSESSMENT & FUNDAMENTALS (HEX & BITS)

---

## **1. The Initial Assessment**

### **Concept Overview**

* **Initial assessment** is the **preliminary evaluation** at the start of a cyber forensics investigation.
* Goal: **Understand scope, impact, and next steps** before detailed analysis.

---

### **Key Components**

1. **Incident Reporting & Information Gathering**

   * Nature of incident
   * Affected systems
   * Timeline
   * Available indicators of compromise (IOCs)

2. **Scoping the Incident**

   * Identify affected systems, networks, or data
   * Assess impact and criticality

3. **Incident Categorization**

   * Data breach
   * Malware attack
   * Network intrusion
   * Insider threat
   * Unauthorized access

4. **Preservation of Evidence**

   * Isolate systems
   * Secure logs
   * Prevent data alteration

5. **Legal & Regulatory Considerations**

   * Notification requirements
   * Involvement of law enforcement
   * Jurisdiction issues

6. **Resource Allocation**

   * Personnel
   * Tools
   * External experts (if required)

7. **Incident Severity & Impact Assessment**

   * Financial impact
   * Operational impact
   * Reputational risk

8. **Incident Response Plan Review**

   * Check applicability
   * Identify gaps

9. **Preliminary Risk Mitigation**

   * Isolate compromised systems
   * Reset credentials
   * Disconnect affected networks

10. **Stakeholder Communication**

* Management
* Legal
* IT & security teams

📌 **MCQ Trap**

* Initial assessment ≠ forensic analysis
* It happens **before deep investigation**

---

## **2. Incident Notification Checklist**

### **Purpose**

* Ensure **timely, structured, and lawful communication** during an incident.

---

### **Checklist**

1. **Internal Notification**

   * Incident response team
   * IT security & system admins

2. **Senior Management**

   * Incident summary
   * Potential impact
   * Actions taken

3. **Legal Counsel**

   * Legal obligations
   * Reporting requirements

4. **IT & Security Teams**

   * Affected systems
   * Containment steps

5. **Communications / PR Team**

   * Public or media communication
   * Consistent messaging

6. **Data Protection Officer (DPO)**

   * If personal data involved
   * Privacy compliance

7. **External Service Providers**

   * Cloud providers
   * MSSPs
   * Vendors

8. **Insurance Provider**

   * Cyber insurance notification

9. **Regulatory Bodies / Law Enforcement**

   * If legally required
   * Criminal incidents

10. **Other Relevant Parties**

* Customers
* Partners
* Vendors

📌 **MCQ Trap**

* Notification order depends on **incident severity & policy**

---

## **3. Hexadecimal Notation**

### **Definition**

* **Hexadecimal (Hex)** is a **base-16 number system** used to represent binary data.

### **Digits Used**

* `0–9` → values 0–9
* `A–F` → values 10–15

---

### **Decimal ↔ Hex Mapping (Important)**

| Decimal | Hex |
| ------- | --- |
| 10      | A   |
| 11      | B   |
| 12      | C   |
| 13      | D   |
| 14      | E   |
| 15      | F   |

---

### **Key Facts**

* 1 Hex digit = **4 binary bits**
* Example:

  * Binary: `1111` → Hex: `F`

📌 **MCQ Trap**

* Hex is **not base-10**
* Hex is **not encryption**

---

## **4. Practical Bits**

### **Definition**

* A **bit** is the **smallest unit of data**
* Values: **0 or 1**

---

### **Practical Uses of Bits**

1. **Binary Number System**

   * Base-2 representation

2. **Data Storage**

   * Hard disks, SSDs, flash memory

3. **Data Transfer Rates**

   * bps, Kbps, Mbps

4. **Networking**

   * Packet transmission
   * Protocol communication

5. **Bit Manipulation**

   * AND, OR, XOR, shifting

6. **Error Detection**

   * Parity bits
   * CRC

7. **Processor Instructions**

   * Machine-level instructions

8. **Digital Media**

   * Images (pixels)
   * Audio (samples)

📌 **MCQ Trap**

* Bit ≠ Byte
* 1 Byte = **8 bits**

---

## **5. Slight Diversion (Exam Interpretation)**

In PG-DITISS context, **“slight diversion”** usually refers to:

* Brief explanation of **fundamental computing concepts**
* Supporting topics required to understand forensic tools
* Not a core forensic process

📌 **MCQ Trap**

* Diversion topics are **conceptual**, not procedural

---

## **6. What is the Use of Hexadecimal**

### **Why Hexadecimal is Used**

1. **Compact Representation**

   * Shorter than binary
2. **Easy Binary Mapping**

   * 4 bits → 1 hex digit
3. **Human Readability**

   * Easier than long binary strings

---

### **Applications of Hexadecimal**

1. **Memory Addresses**
2. **Hex Editors**
3. **File & Disk Analysis**
4. **Debugging Programs**
5. **System Logs**
6. **Color Codes**

   * HTML: `#FF0000`
7. **Encoding Binary Data**

📌 **MCQ Trap**

* Hex is used for **representation**, not security

---

## **Important Facts / Points for MCQs**

* Initial assessment is **pre-analysis**
* Notification checklist ensures **compliance**
* Hexadecimal = base-16
* A–F represent 10–15
* 1 hex digit = 4 bits
* Bits are fundamental to storage & transmission

---

## **MCQ Pointers / Exam Traps**

* Hex vs Binary vs Decimal
* Initial assessment vs investigation
* Notification vs response
* Bit vs byte
* Hexadecimal ≠ encryption
* Notification checklist ≠ incident response plan

---

## **Corrections / Improvements / Suggested Substitutions**

1. **Hex conversion example correction**

   * Hex `3A` = (3 × 16) + 10 = **58 (decimal)**
2. **Terminology**

   * Use *“initial assessment”* not *preliminary investigation*
3. **Clarification**

   * Hexadecimal is **representation**, not **encoding or encryption**
4. **Exam Tip**

   * Questions often mix **hexadecimal with ASCII or Base64**

