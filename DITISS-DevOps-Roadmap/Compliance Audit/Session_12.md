# Session 9 : Centre for Internet Security (CIS) – Critical Security Controls, CIS Compliance & CIS Benchmarks**

---

## 1. Concept Overview

* **Centre for Internet Security (CIS)** is a **non-profit organization** that develops **globally accepted cybersecurity best practices**.
* CIS provides:

  * **CIS Critical Security Controls (CIS Controls)**
  * **CIS Benchmarks**
  * **CIS Compliance mappings**
* **Goal:** Reduce cyber risk by focusing on **known attack vectors** and **poor cyber hygiene**, which are the root cause of most breaches.

---

## 2. Key Definitions (MCQ-Focused)

* **CIS Controls:**
  A **prioritized set of 18 cybersecurity best practices** designed to **prevent, detect, and respond** to cyber attacks.
* **Implementation Groups (IGs):**
  Categories that help organizations **prioritize CIS Controls based on risk, size, and resources**.
* **CIS Benchmarks:**
  **Secure configuration guidelines** for operating systems, applications, cloud services, and network devices.
* **CIS Compliance:**
  Using CIS Controls and Benchmarks to **meet regulatory and framework requirements** (e.g., NIST, ISO).

---

## 3. Main Content (Organized from PPT)

### A. Why CIS Controls Matter (Exam Angle)

* Cyber attacks are:

  * Automated
  * Sophisticated
  * Costly
* **Primary causes of breaches:**

  * Unpatched software
  * Insecure configurations
  * Mismanaged accounts
  * Lack of asset visibility
* **Important Fact:**
  Implementing **IG1 alone can prevent ~85% of common cyber attacks**.

---

### B. CIS Controls Version 8 (v8)

* Total **18 Controls**
* Focus on:

  * Devices
  * Applications
  * Networks
  * People
* Each control includes:

  * **Intent**
  * **Importance**
  * **Tools**
  * **Safeguards** (specific actionable steps)
* Built on **Defense-in-Depth** principle.
* Mapped with:

  * **NIST**
  * **ISO/IEC**
  * **FISMA**

---

### C. Implementation Groups (IGs)

| Implementation Group        | Target Organizations                         | Key Focus                                            |
| --------------------------- | -------------------------------------------- | ---------------------------------------------------- |
| **IG1 – Essential Hygiene** | Small / Medium organizations                 | Basic protection against non-targeted attacks        |
| **IG2 – Enterprise**        | Organizations with IT teams & sensitive data | Moderate complexity & regulatory data                |
| **IG3 – Specialized**       | Govt, Finance, Critical Infrastructure       | Advanced defense against targeted & zero-day attacks |

**MCQ Line:**

* IGs are **not maturity levels**, they are **risk-based prioritization tiers**.

---

### D. CIS Critical Security Controls (All 18 – One-Liners)

1. **Inventory & Control of Assets**

   * Identify and manage all hardware assets (on-prem, cloud, IoT).

2. **Inventory & Control of Software**

   * Allow only authorized and supported software.

3. **Data Protection**

   * Classify, encrypt, retain, and securely dispose data.

4. **Secure Configuration of Assets & Software**

   * Uses **CIS Benchmarks** to create secure baselines.

5. **Account Management**

   * Manage user, admin, and service accounts; remove dormant accounts.

6. **Access Control Management**

   * Enforce **MFA**, RBAC, ACLs; monitor access logs.

7. **Continuous Vulnerability Management**

   * Regular scanning, patching, and remediation tracking.

8. **Audit Log Management**

   * Centralized logging for detection and forensics.

9. **Email & Web Browser Protections**

   * Email filtering, DNS filtering, phishing protection.

10. **Malware Defenses**

    * Anti-malware with behavioral & heuristic detection.

11. **Data Recovery**

    * Regular backups; follow **3-2-1 rule**.

12. **Network Infrastructure Management**

    * Secure network devices; segmentation; firmware updates.

13. **Network Monitoring & Defense**

    * IDS/IPS, flow logs, real-time alerting.

14. **Security Awareness & Skills Training**

    * Phishing awareness and role-based training.

15. **Service Provider Management**

    * Third-party risk management; SOC 2 reports; audit clauses.

16. **Application Software Security**

    * SAST, DAST, WAF; secure SDLC.

17. **Incident Response Management**

    * Documented IR plan; roles; drills.

18. **Penetration Testing**

    * Simulated attacks to validate controls.

---

### E. CIS Benchmarks (Direct Exam Use)

* **What they are:**
  Prescriptive, **secure configuration standards**.
* **Used in:**

  * Operating Systems (Windows, Linux)
  * Databases
  * Network Devices
  * Cloud platforms (AWS, Azure, GCP)
* **Key Feature:**

  * Provide **secure baseline configurations**
  * Support **configuration drift detection**
* **Mapped to Control:**

  * Primarily **Control 4 – Secure Configuration**

---

### F. CIS Compliance

* CIS Controls help organizations:

  * Achieve compliance with:

    * **NIST CSF**
    * **ISO/IEC 27001**
    * **FISMA**
  * Reduce audit gaps
* **Important:**
  CIS is **not a regulation**, but a **recognized best-practice framework**.

---

## 4. Important Facts / Points for MCQs

* Total CIS Controls (v8): **18**
* IG1 prevents approx. **85% of common attacks**
* CIS Benchmarks focus on **secure configuration**
* CIS Controls follow **Defense-in-Depth**
* IGs are based on **risk profile**, not organization size alone
* **3-2-1 Backup Rule:**
  3 copies, 2 media types, 1 off-site/offline

---

## 5. Examples (Exam-Relevant)

* Using **CIS Benchmark for Windows Server** → Control 4
* Enforcing **MFA for remote access** → Control 6
* Conducting **penetration testing annually** → Control 18
* Asking vendors for **SOC 2 reports** → Control 15

---

## 6. MCQ Pointers / Exam Traps

* ❌ CIS Controls ≠ CIS Benchmarks
* ❌ IGs ≠ maturity levels
* ✔ CIS Controls are **prioritized**, not random
* ✔ Secure Configuration control explicitly references **CIS Benchmarks**

---
✅ **Exam Tip:**
For PG-DITISS, remember **numbers (18 controls, 3 IGs)**, **keywords (IG1, Benchmarks, Defense-in-Depth)**, and **control-purpose mapping** — these are high-frequency MCQ areas.
