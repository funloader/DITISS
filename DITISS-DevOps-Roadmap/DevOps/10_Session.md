## ☁️ **Session 10: Cloud Computing Fundamentals, Architecture & Advanced Concepts**

---

### 🧠 **1. Concept Overview**

* **Cloud Computing** delivers **on-demand computing resources** over the internet.
* Resources are **owned and managed by cloud providers**, not end users.
* Enables **scalability, flexibility, cost optimization**, and rapid deployment.

---

### 📖 **2. Key Definitions**

* **Cloud Computing (NIST):**
  A model for enabling **ubiquitous, on-demand network access** to a shared pool of configurable resources.
* **SPI Model:** Service classification – **SaaS, PaaS, IaaS**
* **SLA (Service Level Agreement):** Formal contract defining service availability, performance, and responsibilities.
* **IAM (Identity & Access Management):** Controls **authentication and authorization** of cloud users.

---

### 🧩 **3. Main Content (Organized from Notes)**

---

#### 🌐 **Introduction to Cloud Computing**

* Eliminates need for **on-premise hardware**
* Users pay only for **resources consumed**
* Supports global access and collaboration

---

#### 📌 **Essential Characteristics of Cloud (NIST)**

* On-demand self-service
* Broad network access
* Resource pooling
* Rapid elasticity
* Measured service

---

#### 🧱 **Cloud Deployment Models**

| Model             | Description                                 | Exam Hint    |
| ----------------- | ------------------------------------------- | ------------ |
| **Public Cloud**  | Services offered over internet by providers | Less control |
| **Private Cloud** | Dedicated cloud for single organization     | More secure  |
| **Hybrid Cloud**  | Combination of public + private             | Most common  |

---

#### 🔐 **Cloud Security**

* **SLA** defines uptime, penalties, support
* **IAM** manages:

  * Users
  * Roles
  * Permissions
* Security responsibility is **shared** between provider and customer

---

#### 🏗️ **Cloud Architecture**

* Combination of **SOA + EDA**
* Divided into:

  * **Frontend** – User interface (browser, apps)
  * **Backend** – Cloud infrastructure

**Backend Components:**

* Application
* Services (SaaS, PaaS, IaaS)
* Runtime cloud (VMs)
* Storage
* Infrastructure
* Management
* Security

---

#### 🧩 **Service Models (SPI Model)**

| Model    | Description                  | User Controls |
| -------- | ---------------------------- | ------------- |
| **IaaS** | Virtualized hardware         | OS, apps      |
| **PaaS** | Platform for app development | Code only     |
| **SaaS** | Ready-to-use applications    | No infra      |

**Examples:**

* IaaS → AWS EC2
* PaaS → Google App Engine
* SaaS → Google Docs

---

#### 🧰 **Services Provided by Cloud**

* **Compute** – Virtual machines, serverless
* **Storage** – Object, block, file storage
* **Database** – SQL & NoSQL
* **Developer Tools** – CI/CD, SDKs
* **Web & Mobile** – Hosting, APIs
* **Media** – Streaming, transcoding
* **Security** – IAM, encryption
* **Integration** – Messaging, queues

---

#### 📐 **Cloud Development Best Practices**

* Design for **scalability**
* Use **stateless applications**
* Automate deployment
* Monitor and log resources
* Implement security from design phase

---

#### 🐧 **Introduction to OpenStack**

* **Open-source cloud platform**
* Used to build **private & public clouds**
* Provides:

  * Compute
  * Storage
  * Networking
* Vendor-neutral alternative to AWS

---

#### 🧠 **HCI (Hyper-Converged Infrastructure)**

* Combines:

  * Compute
  * Storage
  * Networking
  * Virtualization
* Delivered as **single integrated system**

##### 🔄 **HCI vs Cloud**

| Feature     | HCI          | Cloud           |
| ----------- | ------------ | --------------- |
| Location    | On-premise   | Internet-based  |
| Scalability | Limited      | Highly scalable |
| Cost Model  | CapEx        | OpEx            |
| Control     | Full control | Shared          |

---

#### 🌐 **SDN (Software Defined Networking)**

* Separates:

  * **Control plane**
  * **Data plane**
* Network managed using **software controllers**
* Enables automation and flexibility

**Benefits:**

* Faster deployment
* Vendor independence
* Reduced operational cost

---

### 🎯 **4. Important Facts / Points for MCQs**

* Cloud follows **pay-as-you-go**
* SLA ≠ IAM
* IaaS gives maximum control
* SaaS hides infrastructure completely
* Hybrid cloud is most adopted
* SDN separates control & data plane
* OpenStack is open-source cloud OS

---

### 🧪 **5. Examples**

* Netflix → Public cloud usage
* Banking → Private cloud
* AWS EC2 → IaaS
* Google Docs → SaaS
* OpenStack → Private cloud setup
* SDN → Network automation

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* Deployment model ≠ Service model
* SLA is contractual, not technical
* IAM is security, not monitoring
* HCI is not cloud (on-prem)
* SDN ≠ NFV (often confused)
* PaaS users cannot manage OS

---

✅ **Exam Priority Reminder:**

> *Expect MCQs on cloud models, SPI differences, SLA vs IAM, OpenStack purpose, HCI vs Cloud, and SDN concepts.*
