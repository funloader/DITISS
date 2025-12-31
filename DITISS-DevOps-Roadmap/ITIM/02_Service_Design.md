# ✍️ ITIL: Service Design — Session 2

**Duration:** 2 Theory Hours
**Module:** IT Infrastructure Management (ITIM)
**Objective:** To understand the principles and processes involved in **designing new or changed IT services** and service management practices, ensuring they meet current and future business requirements.

---

## 📘 **Theory Checklist**

### 🧩 Design Fundamentals
- [x] **Service Design** Principles: Design of architecture, processes, policies, and documentation.
- [x] Design considerations for **future business requirements**.
- [x] Understanding the **Five Aspects of Service Design** (Service Solutions, Management Systems, Tools, Architecture, Metrics/Measurements).

---

### 📦 Key Design Artifacts
- [x] Introduction to the **Service Design Package (SDP)** (The documentation detailing all aspects of the service and its design).
- [x] The purpose and structure of the **Service Catalog Management** process.

---

### 🛡️ Design Processes
- [x] Detailed study of **Service Level Management (SLM)** (Defining, agreeing, and monitoring service targets).
- [x] Designing for **Capacity Management** (Ensuring IT infrastructure can meet current and future performance needs).
- [x] **IT Service Continuity Management (ITSCM)** (Ensuring business continuity after a disaster).
- [x] Principles of **Information Security Management**.

---

## 🧪 **Lab Assignments**

*Note: This session is theory-only according to the syllabus (Sessions 1-5 include 2 hours of Theory only).*

- [ ] **Optional/Discussion:** Analyze a simple service requirement and outline the contents of a **Service Design Package (SDP)** for that service.

---

## 🧰 **Concepts & Frameworks**
- 📦 **Service Design Package (SDP)**
- 📝 **Service Catalog**
- 📈 **Service Level Management (SLM)**
- 🔒 **IT Service Continuity Management (ITSCM)**

---

## 🎯 **Learning Outcomes**
By completing this session, you will:
- ✅ Understand the scope and objectives of the Service Design stage in the ITIL lifecycle.
- ✅ Be able to explain the importance of the Service Design Package (SDP).
- ✅ Be familiar with key design processes including Service Level Management, Capacity Management, and IT Service Continuity.
- ✅ Understand how to design IT services that are aligned with business needs and security requirements.

---

**Title:** **ITIL – Service Design (PG-DITISS – Session 2)**

---

## 1. **Concept Overview**

**Service Design** is a phase of the **ITIL Service Lifecycle** that focuses on **designing IT services, architectures, processes, policies, and documentation** to meet **current and future business requirements**.

🔑 **Key Objective:**
Design services **right the first time** so that they are **cost-effective, secure, scalable, and aligned with business goals** before going live.

---

## 2. **Key Definitions (MCQ-Focused)**

| Term                                | Definition                                                                   |
| ----------------------------------- | ---------------------------------------------------------------------------- |
| **Service Design**                  | Phase where services are designed, agreed, and documented before transition  |
| **Service Design Package (SDP)**    | Complete documentation of all aspects of an IT service through its lifecycle |
| **Service Catalogue**               | Customer-facing list of live IT services                                     |
| **SLA (Service Level Agreement)**   | Formal agreement between service provider and customer                       |
| **SLR (Service Level Requirement)** | Customer’s service expectations                                              |
| **ITSCM**                           | Ensures IT services can be restored after a disaster                         |
| **CIA Triad**                       | Confidentiality, Integrity, Availability                                     |

---

## 3. **Main Content (Aligned to Syllabus)**

---

### 3.1 **Design of Architecture, Processes, Policies & Documentation**

Service Design ensures:

* **Architecture Design**

  * Infrastructure layout
  * Application & technology design
  * Scalability for future demand

* **Process Design**

  * Well-defined ITSM processes
  * Roles & responsibilities defined
  * Integration with other lifecycle stages

* **Policy Design**

  * Security policies
  * Supplier & capacity policies
  * Compliance requirements

* **Documentation**

  * Service Design Package (SDP)
  * SLAs, OLAs, UCs
  * Service Catalogue entries

🎯 **MCQ Line:**

> Service Design ensures *services are not live but fully agreed and documented*.

---

### 3.2 **Service Design Package (SDP)**

**Definition:**
A **comprehensive document** describing **all aspects of an IT service** throughout its lifecycle.

**SDP Includes:**

* Service description
* Functional & non-functional requirements
* SLA, SLR, OLA references
* Capacity, availability & security plans
* Continuity & recovery details
* Cost & supplier information

📌 **Exam Tip:**
SDP is created in **Service Design**, used in **Service Transition**.

---

### 3.3 **Service Catalogue Management**

**Purpose:**

* Maintain a **single source of truth** for all live services
* Acts as a **basis for SLA definition**

**Key Points:**

* Subset of **Service Portfolio**
* Lists **customer-visible services**
* Helps in:

  * Manpower planning
  * SLA negotiation
  * Service request handling

**Catalogue Contains:**

* Service name & description
* Service status
* SLA references
* Service owner

🧠 **MCQ Trap:**
Service Catalogue ≠ Service Portfolio
(Catalogue = live services only)

---

### 3.4 **Service Level Management (SLM)**

**Definition:**
Ensures **agreed service quality levels** are achieved and maintained.

**Core Activities:**

* Negotiating SLAs
* Defining & documenting service levels
* Monitoring & measuring performance
* Reporting service achievements
* Reviewing services with customers

**Objectives:**

* Align IT services with business needs
* Improve service quality
* Act as driver for CSI

**Key Documents:**

* SLR
* SLA
* OLA
* UC
* Service Level Reports
* Service Improvement Plan (SIP)

📌 **Exam Line:**

> SLA defines *what* is delivered, OLA defines *how internally* it is supported.

---

### 3.5 **Designing for Capacity Management**

**Definition:**
Ensures **right capacity, at right time, at right cost**.

**Focus Areas:**

* Current demand
* Future business growth
* Cost optimization

**Activities:**

* Predictive analysis
* Capacity planning
* Real-time monitoring

🎯 **Goal:**
Balance **performance vs cost**

---

### 3.6 **IT Service Continuity Management (ITSCM)**

**Definition:**
Ensures IT services can be **restored within agreed timescales** after disruptions.

**Supports:**
➡ **Business Continuity Management (BCM)**

**Key Concepts:**

* Business Impact Analysis (BIA)
* Recovery Time Objectives (RTO)
* Disaster recovery planning

**ITSCM Lifecycle:**

1. Plan for disaster
2. Agree & approve plans
3. Test regularly
4. Execute during disaster
5. Record actions
6. Analyze & improve

📌 **Exam Point:**
ITSCM focuses on **IT services**, BCM focuses on **entire business**.

---

### 3.7 **Information Security Management**

**Purpose:**
Protect organizational information assets.

**CIA Triad:**

* **Confidentiality:** Authorized access only
* **Integrity:** Accurate & unaltered data
* **Availability:** Accessible when needed

**Key Responsibilities:**

* Define security policies
* Ensure compliance
* Integrate security into service design

🧠 **MCQ Favorite:**
Information Security is a **Service Design process**, not Service Operation.

---

## 4. **Important Facts / Points for MCQs**

* Service Design = **Planning & agreement phase**
* Services are **not live** in this phase
* SDP is the **key output**
* Service Catalogue is **customer-facing**
* SLA is external, OLA is internal
* ITSCM is driven by **BIA**
* Capacity Management balances **cost vs performance**
* CIA triad = core of information security

---

## 5. **Examples (Exam-Friendly)**

* **Capacity Management:** Adding servers before peak banking hours
* **ITSCM:** DR site for core banking application
* **Information Security:** Role-based access for HR systems
* **Service Catalogue:** Internet Banking, ATM Services

---

## 6. **MCQ Pointers / Exam Traps**

⚠ Common Confusions:

* Service Catalogue ≠ Service Portfolio
* SLA ≠ OLA ≠ UC
* ITSCM ≠ Incident Management
* Service Design ≠ Service Transition

---
