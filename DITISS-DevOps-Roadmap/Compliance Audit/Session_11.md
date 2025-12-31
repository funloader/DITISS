# Session 11 : Payment Card Industry Data Security Standard (PCI DSS),  History, Different Levels of PCI
---

## 1. Concept Overview

* **PCI DSS (Payment Card Industry Data Security Standard)** is a **globally recognized, mandatory information security standard**.
* Designed to **reduce credit card fraud** and **protect cardholder data (CHD)**.
* Applies to **any organization that accepts, stores, processes, or transmits payment card data**.
* Managed by the **PCI Security Standards Council (PCI SSC)**.

---

## 2. Key Definitions

* **PCI DSS**: A global security standard for protecting payment card data.
* **Cardholder Data (CHD)**: Primary Account Number (PAN), cardholder name, expiry date.
* **Sensitive Authentication Data (SAD)**: CVV/CVC, PIN, magnetic stripe data (must NOT be stored).
* **CDE (Cardholder Data Environment)**: Systems, networks, and processes that store/process/transmit CHD.
* **QSA (Qualified Security Assessor)**: Authorized external auditor for PCI compliance.
* **ASV (Approved Scanning Vendor)**: Vendor approved to perform vulnerability scans.

---

## 3. Main Content (Organized from PPT)

### A. Purpose & Goals of PCI DSS

* **Protect cardholder data** from unauthorized access
* **Reduce fraud risk** and financial losses
* **Ensure uniform global security requirements**

---

### B. Applicability (Who Must Comply?)

* **Merchants**: Any business accepting credit cards (online or physical).
* **Service Providers**: Payment gateways, hosting providers, processors.
* **Financial Institutions**: Banks, card issuers, processors.
* **Golden Rule**: *If you touch cardholder data, PCI DSS applies to you.*

---

### C. History of PCI DSS (Exam-Oriented Timeline)

| Year         | Event                                         |
| ------------ | --------------------------------------------- |
| Pre-2004     | Each card brand had its own security standard |
| Dec 2004     | **PCI DSS v1.0 released**                     |
| 2006         | **PCI Security Standards Council formed**     |
| 2010–2018    | Versions 1.1, 1.2, 2.0, 3.x                   |
| 2022         | PCI DSS v4.0 released                         |
| Apr 1, 2024  | **PCI DSS v4.0 officially released**          |
| Mar 31, 2025 | **All v4.0 requirements mandatory**           |

---

### D. PCI Security Standards Council (PCI SSC)

* **Established**: September 2006
* **Founding Members (5)**:

  * Visa Inc.
  * MasterCard
  * American Express
  * Discover Financial Services
  * JCB International
* **Role**: Develop, manage, and update PCI standards

---

### E. PCI DSS Framework

* **12 Requirements**
* Grouped into **6 Control Objectives**

#### 6 Control Objectives with Requirements

| Control Objective                        | Requirements                                                                                                                                     |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Build & Maintain Secure Network**      | **Req 1. Network Security Controls** – Firewalls, segmentation<br>**Req 2. No Vendor Defaults** – Change default passwords & settings            |
| **Protect Cardholder Data**              | **Req 3. Protect Stored Cardholder Data** – Encryption, tokenization<br>**Req 4. Encrypt Data in Transmission** – TLS 1.2+                       |
| **Maintain Vulnerability Management**    | **Req 5. Protect Against Malware** – Anti-malware controls<br>**Req 6. Secure Systems & Applications** – Patching, secure SDLC                   |
| **Implement Strong Access Control**      | **Req 7. Restrict Cardholder Data Access** – Need-to-know<br>**Req 8. Multi-Factor Authentication (MFA)**<br>**Req 9. Physical Access Controls** |
| **Monitor & Test Networks**              | **Req 10. Logging & Monitoring** – Audit logs, SIEM<br>**Req 11. Testing & Validation** – Scans, penetration testing                             |
| **Maintain Information Security Policy** | **Req 12. Information Security Policy** – Policies, training, IR, vendor mgmt                                                                    |

---

### F. 12 PCI DSS Requirements (High-Yield Summary)

1. **Network Security Controls** – Firewalls, segmentation
2. **No Vendor Defaults** – Change default passwords/configs
3. **Protect Stored CHD** – Encrypt, tokenize, truncate
4. **Encrypt Data in Transit** – TLS 1.2+
5. **Protect Against Malware** – Anti-malware, assessments
6. **Secure Systems & Applications** – Patching, secure SDLC
7. **Restrict Access** – Need-to-know, RBAC
8. **MFA** – Mandatory for CDE access (Mar 2025+)
9. **Physical Security** – Badge access, CCTV
10. **Logging & Monitoring** – SIEM, 1-year log retention
11. **Testing & Validation** – Quarterly scans, annual pentest
12. **Security Policy** – Training, IR plan, vendor management

---
<details>
<summary><strong>12 PCI DSS Requirements in Detail (dropdown) 🔽 </strong></summary>

### 🔐 **Requirement 1: Network Security Controls**

🎯 **Objective:** Install and maintain network security controls (firewalls, VPNs, cloud-based protections)

• 🔍 Identify all network flows and approved services/protocols
• 🔥 Implement firewalls for all network segments
• ☁️ Cover cloud, virtualized, and traditional environments
• 📄 Document and enforce network segmentation

🌐 **Network Security Firewall Architecture**

---

### 🔑 **Requirement 2: No Vendor-Supplied Defaults**

🎯 **Objective:** Change all vendor-supplied default passwords and security parameters

• 🔐 Change default passwords before network deployment
• 🚫 Disable unnecessary protocols and services
• 📝 Document all security parameters
• 🖥️ Apply to all devices: routers, switches, servers, databases

---

### 🗄️ **Requirement 3: Protect Stored Cardholder Data**

🎯 **Objective:** Protect stored cardholder data through encryption or other controls

• 🔒 Encrypt data at rest using AES-256 or AES-128
• ✂️ Truncate, tokenize, or hash card data
• 🔑 Implement strong key management (RSA 2048 or higher)
• ⏳ Reduce data retention periods

🔐 **Data Encryption – Secure Implementation**

---

### 📡 **Requirement 4: Encrypt Data in Transmission**

🎯 **Objective:** Protect cardholder data transmitted across public networks

• 🔐 Use TLS 1.2 or higher for all transmissions
• 🌐 Implement SSL/TLS on all public networks
• 📶 Encrypt wireless transmissions
• ❌ Phase out weak encryption standards

---

### 🦠 **Requirement 5: Protect Against Malware**

🎯 **Objective:** Deploy anti-malware solutions and conduct regular assessments

• 🛡️ Install anti-malware on all vulnerable systems
• 💽 Scan removable media for malware
• 📅 Conduct annual malware risk assessments
• 🔄 Maintain current anti-malware definitions

---

### 🧩 **Requirement 6: Secure Systems & Applications**

🎯 **Objective:** Develop and maintain secure systems and applications

• 🧑‍💻 Establish secure software development practices
• ⬆️ Install all security patches promptly
• 🧪 Conduct code reviews and penetration testing
• 🧾 Implement payment page script security controls

---

### 🚦 **Requirement 7: Restrict Cardholder Data Access**

🎯 **Objective:** Restrict access to cardholder data on a need-to-know basis

• 🧑‍💼 Implement role-based access control (RBAC)
• 🔐 Grant minimum necessary permissions
• 📝 Document all access authorizations
• 🔁 Review access periodically (at least quarterly)

---

### 🔑📲 **Requirement 8: Multi-Factor Authentication (MFA)**

🎯 **Objective:** Ensure user identity verification through MFA

• ⏰ Mandatory (March 2025+): MFA for ALL CDE access
• 🔠 Minimum 12-character passwords
• 🛡️ Implement MFA for admins and remote access
• ❌ No default credentials

---

### 🏢 **Requirement 9: Physical Access Controls**

🎯 **Objective:** Restrict physical access to cardholder data resources

• 🎫 Use badge readers and video surveillance
• 📋 Maintain visitor access logs
• 🗄️ Secure data centers and server rooms
• 💾 Protect portable media devices

---

### 📊 **Requirement 10: Logging & Monitoring**

🎯 **Objective:** Maintain audit logs and monitor access to cardholder data

• 🧾 Log all access to cardholder data
• 🤖 Implement automated log reviews
• 🕒 Retain logs for minimum 1 year
• 📡 Implement SIEM for real-time monitoring

---

### 🧪 **Requirement 11: Testing & Validation**

🎯 **Objective:** Regularly test and validate security systems

• 🔍 Quarterly vulnerability scans (internal & external)
• 🧨 Annual penetration testing
• 🌐 Web Application Firewall testing
• 📶 Quarterly wireless access point scanning

---

### 📜 **Requirement 12: Information Security Policy**

🎯 **Objective:** Maintain comprehensive information security policy

• 📝 Document security policies and procedures
• 🎓 Conduct annual security awareness training
• 🚨 Include incident response procedures
• 🤝 Manage third-party/vendor compliance

</details>

---

### G. PCI DSS v4.0 – Key Exam Highlights

* **64 new requirements**
* **Mandatory MFA for ALL CDE access (March 2025)**
* **Minimum password length: 12 characters**
* **Risk-based & continuous compliance approach**
* Stronger vulnerability remediation requirements

---

### H. Different Levels of PCI (Merchant Levels)

| Level       | Transactions per Year        | Validation Requirement                  |
| ----------- | ---------------------------- | --------------------------------------- |
| **Level 1** | > 6 million                  | Annual ROC by QSA + Quarterly ASV scans |
| **Level 2** | 1–6 million                  | Annual SAQ + Quarterly ASV scans        |
| **Level 3** | 20k–1M e-commerce            | Annual SAQ + Quarterly ASV scans        |
| **Level 4** | < 20k e-commerce / ≤1M total | Annual SAQ (+ scans if applicable)      |

> **Level 1 = Highest & most stringent**

---

## 4. Important Facts / Points for MCQs

* PCI DSS is **mandatory**, not optional
* PCI DSS has **12 requirements & 6 control objectives**
* **PCI SSC ≠ Regulator**, but manages the standard
* **SAD must never be stored**
* **TLS 1.2+** required for data transmission
* **AES-128/256** for encryption at rest
* **RSA 2048+** for key management
* Logs must be retained for **minimum 1 year**
* MFA mandatory from **March 31, 2025**

---

## 5. Examples (Exam-Relevant)

* **Amazon / Flipkart** → Merchant (Level 1)
* **Razorpay / PayU** → Service Provider
* **Bank issuing credit cards** → Financial Institution
* **Small online store (<20k txns)** → Level 4 Merchant

---

## 6. MCQ Pointers / Exam Traps

* ❌ PCI DSS applies only to banks → **Wrong**
* ❌ PCI DSS is optional → **Wrong**
* ❌ SAD can be encrypted & stored → **Wrong**
* PCI DSS ≠ ISO 27001 (ISO is voluntary, PCI is mandatory)
* PCI DSS v4.0 MFA deadline = **March 2025**
* **Merchant level ≠ Security maturity**, based on **transaction volume**
* ROC is required **only for Level 1 merchants**

---

