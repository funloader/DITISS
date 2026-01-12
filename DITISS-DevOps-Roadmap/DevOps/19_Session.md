## ☁️ **Session 19: AWS Fundamentals, Core Services & VPC Basics**

---

### 🧠 **1. Concept Overview**

* **AWS (Amazon Web Services)** is a **public cloud platform** providing on-demand infrastructure and services.
* Offers **IaaS, PaaS, and SaaS** services on a **pay-as-you-go** model.
* Session focuses on **core AWS services** and **basic networking using VPC**.

---

### 📖 **2. Key Definitions**

* **AWS:** Cloud service provider offering scalable compute, storage, and networking services.
* **EC2 (Elastic Compute Cloud):** Virtual servers in the AWS cloud.
* **Lambda:** Serverless compute service.
* **S3 (Simple Storage Service):** Object storage service.
* **VPC (Virtual Private Cloud):** Logically isolated virtual network in AWS.

---

### 🧩 **3. Main Content (Organized from Notes)**

---

#### 🔰 **Introduction to AWS**

* Provides:

  * Compute
  * Storage
  * Networking
  * Security
* Global infrastructure with:

  * Regions
  * Availability Zones (AZs)

📌 *AWS follows shared responsibility model.*

---

#### 🧰 **AWS Core Services**

##### 🖥️ **EC2**

* Provides resizable **virtual machines**
* Users control:

  * OS
  * Applications
* Used for:

  * Web servers
  * Application servers

**Key Points:**

* Instance types based on CPU, memory
* Billed per usage

---

##### ⚡ **AWS Lambda**

* **Serverless compute**
* No server management required
* Executes code in response to events

**Key Points:**

* Auto-scaling
* Pay only for execution time
* Used for event-driven applications

---

##### 📦 **Amazon S3**

* **Object storage** service
* Stores data as objects in buckets

**Key Points:**

* Highly durable & scalable
* Used for:

  * Backup
  * Static websites
  * Media storage

---

#### 🌐 **Introduction to VPC Setup**

* VPC provides:

  * Network isolation
* Users define:

  * IP address range (CIDR)
  * Subnets
  * Routing

**Basic VPC Components:**

* Subnets (Public / Private)
* Route Tables
* Internet Gateway
* Security Groups

📌 *Every EC2 runs inside a VPC.*

---

### 🎯 **4. Important Facts / Points for MCQs**

* AWS is **public cloud**
* EC2 = IaaS
* Lambda = Serverless (PaaS)
* S3 = Object storage
* VPC = Logical network isolation
* AWS regions contain multiple AZs

---

### 🧪 **5. Examples**

* EC2 → Hosting web application
* Lambda → Event processing
* S3 → Backup storage
* VPC → Secure application network

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* EC2 ≠ Lambda
* S3 ≠ Block storage
* VPC ≠ Data center
* Region ≠ Availability Zone
* Lambda has execution time limits
* Security Group ≠ Firewall appliance

---

✅ **Exam Priority Tip:**

> *PG-DITISS MCQs often test AWS service use-cases, EC2 vs Lambda vs S3 differences, and basic VPC components—revise definitions and traps carefully.*
