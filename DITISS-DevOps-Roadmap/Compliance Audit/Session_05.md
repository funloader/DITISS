# General Data Protection Regulation (GDPR) – Overview, Types of Privacy Data & Key Compliance Steps

---

## 1. Concept Overview

* **GDPR (General Data Protection Regulation)** is the **EU’s comprehensive data protection law** governing the **processing of personal data**.
* Enforced from **25 May 2018**
* Objective:

  * Protect **fundamental rights and freedoms** of individuals
  * Ensure **uniform data protection law across EU**
  * Regulate how organizations **collect, use, store, and share personal data**

---

## 2. Key Definitions (Highly MCQ-Relevant)

| Term                                                | Definition                                                                   |
| --------------------------------------------------- | ---------------------------------------------------------------------------- |
| **Personal Data**                                   | Any information relating to an **identified or identifiable natural person** |
| **Sensitive Personal Data / Special Category Data** | Data requiring **higher protection** (health, biometrics, religion, etc.)    |
| **Processing**                                      | Any operation on data (collection, storage, use, transfer, deletion)         |
| **Data Subject**                                    | Individual whose personal data is processed                                  |
| **Controller**                                      | Entity deciding **purpose & means** of processing                            |
| **Processor**                                       | Entity processing data **on behalf of controller**                           |
| **Pseudonymisation**                                | Data can be re-identified using additional information                       |
| **Anonymisation**                                   | Irreversible process; data no longer personal data                           |

---

## 3. Main Content (Organized from PPT)

### A. GDPR – Overview

#### Origins & Background (Exam-Friendly Timeline)

* **1949** – Council of Europe established
* **1951** – ECSC → later EU
* **1970s–80s** – Early privacy laws due to computers & telecom
* **1981** – Council of Europe Convention (first binding data protection treaty)
* **1995** – EU Data Protection Directive (95/46/EC)
* **2000s** – Identity thefts, e-commerce growth
* **2010s** – Social media, cloud, online advertising
* **2018** – GDPR enforced

---

### B. Types of Privacy Data Protected under GDPR

#### 1. Personal Data (Article 4)

Examples:

* Name, address, email
* Aadhaar/Passport number
* IP address, device IDs
* Location data

#### 2. Special Category (Sensitive) Data (Article 9)

Includes:

* Health & medical data
* Biometric & genetic data
* Racial or ethnic origin
* Political opinions
* Religious or philosophical beliefs
* Sexual orientation

> [!IMPORTANT]
>**Processing generally prohibited unless specific conditions apply**

#### 3. Pseudonymous vs Anonymous Data

| Aspect                 | **Pseudonymous Data**                                                                                                            | **Anonymous Data**                                                       |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Meaning**            | Personal data where identifiers are **replaced with a code**, but **re-identification is possible** using additional information | Data processed in such a way that **individual can never be identified** |
| **GDPR Applicability** | ✅ **GDPR applies**                                                                                                               | ❌ **GDPR does NOT apply**                                                |
| **Re-identification**  | **Possible** (via key / mapping table)                                                                                           | **Not possible**                                                         |
| **Link to individual** | Indirect but exists                                                                                                              | Completely removed                                                       |
| **Legal Status**       | Still considered **personal data**                                                                                               | Not personal data                                                        |
| **Security Level**     | Reduced risk, not zero risk                                                                                                      | No privacy risk                                                          |
| **Typical Use**        | Analytics, research, testing                                                                                                     | Public statistics, reports                                               |

---

### C. Key GDPR Principles (Article 5)

| Principle                       | Meaning                                |
| ------------------------------- | -------------------------------------- |
| **Lawfulness & Fairness**       | Processing must have valid legal basis |
| **Purpose Limitation**          | Use data only for specified purpose    |
| **Data Minimization**           | Collect only necessary data            |
| **Accuracy**                    | Keep data correct & updated            |
| **Storage Limitation**          | Retain only as long as required        |
| **Integrity & Confidentiality** | Ensure security of data                |
| **Accountability**              | Controller must demonstrate compliance |

---

### D. Lawful Bases for Processing (Article 6)

1. Consent
2. Contractual necessity
3. Legal obligation
4. Vital interests
5. Public interest / official authority
6. Legitimate interests

> [!IMPORTANT]
> **Consent must be: freely given, specific, informed, unambiguous**

---

### E. Rights of Data Subjects (Very Important for MCQs)


* **Right to Access (Article 15)**
  → Data subject can **obtain confirmation**, **copy of personal data**, and details of processing.

* **Right to Rectification (Article 16)**
  → Data subject can **correct inaccurate** or **complete incomplete** personal data.

* **Right to Erasure / Right to be Forgotten (Article 17)**
  → Data subject can request **deletion of personal data** when it is no longer necessary, consent is withdrawn, or processing is unlawful.

* **Right to Restriction of Processing (Article 18)**
  → Data subject can **limit processing** while accuracy or legality is contested.

* **Right to Object (Article 21)**
  → Data subject can **object to processing** based on legitimate interests or direct marketing.

* **Right to Withdraw Consent (Article 7)**
  → Data subject can **withdraw consent at any time**, without affecting past lawful processing.

* **Right to Data Portability (Article 20)**
  → Data subject can **receive and transfer personal data** in a **structured, commonly used, machine-readable format**.

* **Rights Related to Automated Decision-Making & Profiling (Article 22)**
  → Data subject has the **right not to be subject to decisions based solely on automated processing**, including profiling, that produce legal or significant effects.

---

### F. Security & Accountability Requirements

* **Appropriate technical & organizational measures**
* **Data breach notification**:

  * To authority within **72 hours**
* **Data Protection by Design & by Default**
* **Data Protection Impact Assessment (DPIA)** – mandatory for high-risk processing
* **Data Protection Officer (DPO)** – mandatory in certain cases

---

### G. International Data Transfers

Allowed only via:

* **Adequacy decisions**
* **Standard Contractual Clauses (SCCs)**
* **Binding Corporate Rules (BCRs)**
* Codes of conduct & certifications
* Specific **derogations**

> [!IMPORTANT]
>**Safe Harbor & Privacy Shield are invalidated**

---

### H. Penalties & Enforcement

* Supervisory Authorities + European Data Protection Board (EDPB)
* Fines:

  * Up to **€20 million OR 4% of global annual turnover** (whichever is higher)
* Data subjects can claim **compensation**

---

## 4. Important Facts / Points for MCQs

* GDPR applies to **EU and non-EU organizations** processing EU residents’ data
* Applies to **controllers and processors**
* **Territorial scope** includes companies offering goods/services to EU citizens
* GDPR replaced **Data Protection Directive 95/46/EC**
* **Breach notification timeline: 72 hours**

---

## 5. Examples (Exam-Oriented)

* Indian IT company processing EU customer data → **GDPR applicable**
* Health records of EU citizens → **Special category data**
* Email marketing without consent → **Violation**
* CCTV footage with identifiable faces → **Personal data**

---
## 6. **GDPR Terms Explained – Controller, Joint Controller & Processor (MCQ-Focused)**

---

### **1. Data Controller (Article 4(7))**

**Meaning:**
→ A **natural or legal person, public authority, agency, or body** which **determines the purposes and means** of processing personal data.

**Key Points for MCQs:**

* Decides **WHY** and **HOW** data is processed
* Has **primary responsibility** for GDPR compliance
* Can be **single or multiple controllers**

**Example:**

* An e-commerce company deciding to collect customer data for order delivery and marketing

---

### **2. Joint Controllers (Article 26)**

**Meaning:**
→ Two or more controllers who **jointly determine the purposes and means** of processing.

**Key Points for MCQs:**

* **Shared decision-making**
* Must define responsibilities via **joint controller arrangement**
* Data subjects can exercise rights **against any joint controller**

**Example:**

* Facebook and a business page jointly deciding how user data is collected and used for analytics

---

### **3. Data Processor (Article 4(8))**

**Meaning:**
→ A person or entity which **processes personal data on behalf of the controller**.

**Key Points for MCQs:**

* Processes data **only on controller’s instructions**
* Does **not decide purpose**
* Must follow **data processing agreement (DPA)**

**Example:**

* Cloud service provider storing customer data for a company

---

### **Controller vs Joint Controller vs Processor (Comparison Table)**

| Aspect               | Controller | Joint Controller | Processor |
| -------------------- | ---------- | ---------------- | --------- |
| Decides purpose      | ✔ Yes      | ✔ Yes (jointly)  | ❌ No      |
| Decides means        | ✔ Yes      | ✔ Yes (jointly)  | ❌ No      |
| Acts on instructions | ❌          | ❌                | ✔         |
| Primary liability    | ✔          | ✔ (shared)       | Limited   |
| Agreement required   | Optional   | Mandatory        | Mandatory |

---

## **One-Liners for MCQs**

* **Controller decides “why & how”**
* **Processor acts “on behalf of”**
* **Joint controllers share decisions and responsibility**
* **Processor ≠ controller even if it processes data**

---

## 7. MCQ Pointers / Exam Traps

* ❌ Anonymous data ≠ Pseudonymous data
* ❌ Consent is **not the only legal basis**
* ✔ GDPR covers **online identifiers** (IP, cookies)
* ✔ Legitimate interest cannot override fundamental rights
* ❌ Privacy Shield is **NOT valid**
* ✔ Right to be Forgotten ≠ absolute right
* ❌ Processor can decide purpose → **False**
* ❌ Joint controllers = controller + processor → **False**
* ✔ A processor can become a controller if it determines purpose → **True**

---
