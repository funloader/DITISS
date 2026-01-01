# SESSION 2 – COMPUTER FORENSICS 🖥️🔍

---

## **1. Computer Forensics Involves** 🧪⚖️

Computer Forensics is the scientific process of **collecting, preserving, analyzing, and presenting digital evidence** in a legally admissible manner.

### It Involves:

* Identification of digital evidence 🆔
* Preservation without alteration 🛡️
* Extraction using forensic tools 🧰
* Documentation of every action 📝
* Interpretation of findings for legal use ⚖️

🔹 **Key Objective:** Maintain **integrity, authenticity, and admissibility** of evidence ✅

---

## **2. Preservation** 🛡️💾

Preservation ensures that **digital evidence remains unchanged** from the moment of seizure.

### Key Points:

* Use **write blockers** to prevent modification 🚫✍️
* Create **bit-by-bit forensic images** 📀
* Maintain **hash values** (MD5 / SHA-256) 🔑
* Store evidence in **secure, controlled environments** 🔒

📌 **MCQ Trap:**
Preservation ≠ Analysis ❌
Preservation happens **before** examination ⏳

---

## **3. Identification** 🔎📁

Identification is the process of **locating potential sources of digital evidence**.

### Sources Include:

* Hard disks, SSDs, USB drives 💽
* RAM (volatile data) ⚡
* Logs, emails, browser history 📧🌐
* Network traffic 🌐
* Mobile, IoT, Cloud data 📱☁️

📌 **MCQ Point:**
Identification answers **“WHAT evidence exists and WHERE”**, not “HOW it happened” ❓

---

## **4. Extraction** 📤🛠️

Extraction refers to **retrieving data from identified sources** using forensic techniques.

### Types:

* **Static extraction:** From powered-off devices 🔌
* **Live extraction:** From running systems (RAM, processes) ⚡

### Methods:

* Disk imaging 💿
* Memory dumps 🧠
* Log extraction 📜
* File carving ✂️

⚠️ **Exam Note:**
Live extraction must be **quick** due to volatility ⏱️

---

## **5. Documentation** 📝📚

Documentation is the **most critical legal component** of forensic investigation.

### Includes:

* Date & time of actions ⏰
* Tools and versions used 🧰
* Hash values 🔐
* Investigator details 👤
* Evidence movement logs 🚚

📌 **MCQ Favorite:**
Poor documentation → **Evidence inadmissible in court** ⚖️❌

---

## **6. Interpretation** 📊🧠

Interpretation converts **technical findings into understandable conclusions**.

### Includes:

* Timeline reconstruction ⏳
* Event correlation 🔗
* Attack pattern analysis 🧬
* Linking suspect actions to evidence 🧩

🔹 Used for:

* Court testimony ⚖️
* Incident reports 📄
* Management decisions 👔

---

## **7. Goals of Forensics Analysis** 🎯🔍

Primary goals include:

1. **Preserve evidence integrity** 🛡️
2. **Reconstruct events** ⏳
3. **Identify attacker / actions** 🕵️‍♂️
4. **Support legal proceedings** ⚖️
5. **Prevent future incidents** 🚨

📌 **MCQ Trap:**
Goal is **not** system recovery — it is **evidence discovery** ❌💻

---

## **8. Types of Cyber Forensics Techniques** 🧑‍💻🔬

### 1. Disk Forensics 💽

* File systems
* Deleted data recovery ♻️

### 2. Memory (Live) Forensics ⚡

* RAM analysis
* Running processes 🧠

### 3. Network Forensics 🌐

* Packet capture 📡
* IDS/Firewall logs 🔥

### 4. Malware Forensics 🦠

* Reverse engineering 🔄
* Behavioral analysis 🧪

### 5. Mobile / IoT / Cloud Forensics 📱☁️

* App data
* Logs
* Virtual instances 🖥️

📌 **MCQ Tip:**
Live forensics = **Volatile data** ⚡

---

## **9. Cyber Forensics Procedures** 📋➡️

Standard procedure follows this order:

1. Preparation 🛠️
2. Identification 🔎
3. Preservation 🛡️
4. Collection 📥
5. Examination 🔍
6. Analysis 📊
7. Documentation 📝
8. Presentation 🎤

⚠️ **MCQ Order Question Alert** 🚨

---

## **10. Preparation** 🧠📦

Preparation occurs **before any incident happens**.

### Includes:

* Policies and SOPs 📑
* Legal approvals ⚖️
* Tool readiness 🧰
* Team training 🎓

📌 **Exam Point:**
Lack of preparation = Delayed & flawed investigation ⏰❌

---

## **11. What to Do Before the Incident** ✅📌

* Develop incident response plan 📘
* Train forensic team 👨‍🏫
* Deploy logging & monitoring 📊
* Establish chain of custody templates 🔗
* Ensure legal compliance ⚖️

---

## **12. Incident Response Plan** 🚨📘

A documented strategy for **handling cyber incidents**.

### Components:

* Incident classification 🗂️
* Response steps 🪜
* Communication flow 📞
* Escalation matrix ⬆️
* Recovery procedures 🔄

📌 **MCQ:**
IR Plan = **Proactive**, not reactive ✅

---

## **13. Incident Response Team** 👥🛡️

A **multidisciplinary team** responsible for incident handling.

### Members:

* Incident Manager 👔
* Forensic Investigator 🕵️
* IT/Security staff 💻
* Legal counsel ⚖️
* PR / Management 📢

⚠️ **Exam Trap:**
Forensics ≠ Only technical team ❌

---

## **14. Detecting Incidents** 🚨🔍

Detection identifies **signs of compromise**.

### Methods:

* IDS / IPS 🛡️
* SIEM 📊
* Log analysis 📜
* EDR 🖥️
* User reports 👤
* Honeypots 🍯

📌 **MCQ:**
Detection precedes **Investigation** ⏳

---

## **15. Chain of Custody** 🔗⚖️

Chain of custody documents **who handled evidence, when, where, and how**.

### Ensures:

* Evidence integrity 🛡️
* Legal admissibility ⚖️
* Accountability 📋

### Includes:

* Transfer records 🚚
* Storage details 🗄️
* Signatures ✍️
* Timestamps ⏰

⚠️ **Most Important MCQ Rule:**
Broken chain = **Evidence rejected in court** ❌⚖️

---

## **EXAM CORRECTIONS / IMPROVEMENTS / SUBSTITUTIONS** 🧠✏️

| Common Mistake          | Correct Concept                 |
| ----------------------- | ------------------------------- |
| Preservation = Backup   | Preservation = Forensic imaging |
| MD5 is secure           | SHA-256 preferred               |
| Analysis before imaging | Imaging always first            |
| No documentation needed | Documentation is mandatory      |
| Live analysis anytime   | Only when justified             |

---

## **LAST-MINUTE MCQ POINTERS** ⏰📌

* Write-blocker prevents **modification** 🚫
* Hash mismatch = **Evidence tampered** ⚠️
* Volatile data = **RAM** ⚡
* Hex editor works at **byte level** 🧮
* Chain of custody is **legal proof** ⚖️
* Forensics ≠ Incident response (but related) 🔍🚨

---
