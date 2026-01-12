## ⚙️ **Session 15 & 16: DevOps Fundamentals, Ecosystem & Core Technologies**

---

### 🧠 **1. Concept Overview**

* **DevOps** is a cultural and technical movement that **integrates Development and Operations**.
* Focuses on **automation, collaboration, continuous delivery**, and faster business value.
* Uses tools, practices, and principles like **CAMS, CI/CD, containers, and virtualization**.

---

### 📖 **2. Key Definitions**

* **DevOps:** A set of practices that combines **software development and IT operations** to shorten the system development life cycle.
* **CAMS Model:** Culture, Automation, Measurement, Sharing.
* **CI/CD:** Continuous Integration & Continuous Delivery/Deployment.
* **Immutable Deployment:** Infrastructure that is **never modified after creation**.

---

### 🧩 **3. Main Content (Organized from Notes)**

---

#### 🔰 **Introduction to DevOps**

* Aims to:

  * Reduce deployment failures
  * Increase deployment frequency
  * Improve recovery time
* Breaks **silos** between Dev & Ops teams

📌 *DevOps is culture + tools + practices.*

---

#### 🌐 **DevOps Ecosystem**

* Collection of:

  * Tools
  * Platforms
  * Practices
* Covers entire software lifecycle

**Ecosystem Components:**

* Version Control
* CI/CD tools
* Configuration Management
* Containers
* Monitoring & Logging
* Cloud platforms

---

#### 🔄 **DevOps Phases**

1. Plan
2. Code
3. Build
4. Test
5. Release
6. Deploy
7. Operate
8. Monitor

📌 *Lifecycle is continuous, not linear.*

---

#### 🧭 **CAMS Model**

* **Culture:** Collaboration & trust
* **Automation:** Reduce manual work
* **Measurement:** Metrics & monitoring
* **Sharing:** Knowledge & responsibility

---

#### ♻️ **Kaizen**

* Japanese philosophy of **continuous improvement**
* Focuses on:

  * Small, incremental changes
* Aligns well with DevOps & Agile

---

#### 🧱 **Immutable Deployment**

* Servers are:

  * Replaced, not updated
* New version → new instance
* Old instances are destroyed

**Benefits:**

* Predictable deployments
* Easy rollback
* Reduced configuration drift

---

#### 🔁 **CI/CD Pipelines**

* Automated process from:

  * Code commit → production
* CI:

  * Build & test automatically
* CD:

  * Deploy automatically

**Benefits:**

* Faster releases
* Fewer errors
* Continuous feedback

---

#### 🔐 **IAM (Identity & Access Management)**

* Controls:

  * Who can access what
* Uses:

  * Users
  * Roles
  * Policies

📌 *Security backbone of DevOps pipelines.*

---

#### 📦 **LXC (Linux Containers)**

* OS-level virtualization
* Lightweight containers
* Shares host OS kernel

---

#### 🐳 **Docker**

* Popular containerization platform
* Packages app + dependencies
* Portable and fast

📌 *Docker uses LXC concepts.*

---

#### 🖥️ **KVM (Kernel-based Virtual Machine)**

* Type 1 hypervisor
* Converts Linux into hypervisor
* Full hardware virtualization

---

### 🎯 **4. Important Facts / Points for MCQs**

* DevOps ≠ Tool
* CAMS = Culture, Automation, Measurement, Sharing
* Immutable deployment ≠ in-place update
* CI runs on every code commit
* CD automates deployment
* Docker ≠ VM
* KVM is a **Type 1 hypervisor**
* IAM controls access

---

### 🧪 **5. Examples**

* Jenkins → CI/CD
* Docker → Containerization
* KVM → Virtual machines
* IAM → Access control
* Blue-Green deployment → Immutable model

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* DevOps ≠ Agile (but complements it)
* CI ≠ CD
* Containers ≠ Virtual Machines
* LXC ≠ Docker (Docker is higher-level)
* Immutable deployment ≠ auto-scaling
* IAM ≠ monitoring

---

✅ **Final Exam Tip:**

> *PG-DITISS MCQs heavily test definitions, differences (VM vs container, CI vs CD, LXC vs Docker), and models like CAMS—revise one-liners and traps carefully.*
