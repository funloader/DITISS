## 📘 **Session 8: Virtualization & Cluster Architecture**

---

### 🧠 **1. Concept Overview**

* **Virtualization** is a technique to **logically divide physical computing resources** into multiple virtual environments.
* Achieved by **abstracting hardware resources** using a software layer called a **hypervisor**.
* Core foundation of **cloud computing** and **DevOps infrastructure**.

---

### 📖 **2. Key Definitions**

* **Virtualization**: Creation of **software-based (virtual) versions** of hardware resources like servers, storage, or networks.
* **Hypervisor**: Software that **creates, runs, and manages virtual machines (VMs)**.
* **Virtual Machine (VM)**: A **software-based computer** running an OS and applications like a physical machine.

---

### 🧩 **3. Main Content (From Notes)**

---

#### 🧱 **Introduction to Virtualization**

* Allows **multiple operating systems** to run on a **single physical machine**.
* Improves:

  * Resource utilization
  * Flexibility
  * Portability
* A VM is stored as a **single data file** → can be moved across systems.

---

#### ⚙️ **Virtualization Types**

##### 🔹 **Type 1 Hypervisor (Bare Metal)**

* Installed **directly on physical hardware**
* No host OS layer
* **Low latency**, **high performance**, **more secure**
* Used in **enterprise & cloud environments**

**Examples:**

* VMware ESXi
* Microsoft Hyper-V
* KVM (Kernel-based Virtual Machine)

---

##### 🔹 **Type 2 Hypervisor (Hosted)**

* Installed **on top of a host operating system**
* Extra OS layer → **higher latency**
* Mostly used for **end-user or testing environments**

**Examples:**

* Oracle VirtualBox
* VMware Workstation

---

#### 🔄 **Virtualization Techniques**

##### 🔸 **Hardware Virtualization**

* Hypervisor interacts **directly with hardware**
* Each VM runs its **own OS**
* High isolation

##### 🔸 **Para-Virtualization**

* Guest OS is **aware of virtualization**
* Requires OS modification
* Better performance than full virtualization

---

#### 📦 **Virtualization Operations**

| Term             | Description                                      |
| ---------------- | ------------------------------------------------ |
| **Template**     | Pre-configured VM image used to create new VMs   |
| **Cloning**      | Creating an **exact copy** of an existing VM     |
| **Snapshot**     | Captures VM state (OS + data) at a point in time |
| **Snapshot Use** | Rollback during failure or testing               |

---

#### 🖥️ **Operating System Virtualization**

* Also called **Containerization**
* Virtualizes **OS-level resources**, not hardware
* Multiple containers share **same host OS kernel**
* Lightweight compared to VMs

**Examples (Exam-relevant):**

* Docker
* LXC

---

#### 🧩 **Cluster Architecture**

* A **cluster** is a group of **independent systems** working together as a **single system**
* Used for:

  * High availability
  * Load balancing
  * Fault tolerance

---

#### 📋 **Cluster Requirements**

* **Multiple Nodes** (Servers)
* **Shared Storage** (SAN / NAS)
* **High-speed Network**
* **Cluster Management Software**
* **Heartbeat / Monitoring mechanism**
* **Failover support**

---

### 🎯 **4. Important Facts / Points for MCQs**

* Virtualization is **hardware abstraction**
* Type 1 hypervisors are **more secure** than Type 2
* Para-virtualization requires **OS modification**
* Containers ≠ VMs (no separate OS per container)
* Snapshot ≠ Clone
* Cluster ≠ Virtualization (different concepts)

---

### 🧪 **5. Examples**

* VMware ESXi → Type 1 Hypervisor
* VirtualBox → Type 2 Hypervisor
* Docker → OS Virtualization
* Snapshot → Before OS upgrade
* Cloning → Creating test VM copies

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* **Type 1 vs Type 2** confusion (installation location)
* **Snapshot vs Backup** (snapshot is not a full backup)
* **Cloning vs Template**
* **Containers share kernel** (VMs do not)
* Para-virtualization ≠ Hardware virtualization
* Cluster improves **availability**, not virtualization

---

✅ **Exam Priority Tip:**

> *PG-DITISS MCQs often test differences, examples, and one-line definitions — revise tables and traps carefully.*
