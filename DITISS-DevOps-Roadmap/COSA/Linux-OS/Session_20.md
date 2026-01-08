## 🖥️ Session 20: Virtual Machine Management & Virtual Machine Network Configuration

---

## 🧠 **1. Concept Overview**

* **Virtualization** allows running **multiple virtual machines (VMs)** on a single physical system.
* Each VM has its **own OS, resources, and network configuration**.
* Commonly used in **server consolidation, testing, cloud, and labs**.
* In PG-DITISS, focus is on **VM management concepts + network modes** (MCQ-heavy).

---

## 📘 **2. Key Definitions**

* **Virtual Machine (VM):**
  A software-based emulation of a physical computer.
* **Hypervisor:**
  Software that creates and manages VMs.
* **Host OS:**
  Physical system running the hypervisor.
* **Guest OS:**
  OS running inside a VM.
* **Virtual Network Adapter:**
  Software-based NIC for VM networking.

---

## 🧩 **3. Main Content (Organized from COSA–Linux context)**

---

## ⚙️ **A. Virtual Machine Management**

### 🔹 What is VM Management?

* Creation, configuration, start/stop, pause, clone, and deletion of VMs.
* Allocation of system resources:

  * CPU
  * RAM
  * Disk
  * Network

---

### 🔹 Hypervisor Types

| Type       | Description | Example                        |
| ---------- | ----------- | ------------------------------ |
| **Type 1** | Bare-metal  | VMware ESXi, KVM               |
| **Type 2** | Hosted      | VirtualBox, VMware Workstation |

📌 **COSA-Linux Context:**

* **VirtualBox** is commonly used for Linux labs.

---

### 🔹 VM Lifecycle Operations

* Create VM
* Start / Stop / Reboot
* Pause / Resume
* Snapshot
* Clone
* Delete

---

### 🔹 VM Resource Management

* **CPU:** vCPU assigned
* **Memory:** Fixed or dynamic RAM
* **Storage:** Virtual Disk (VDI, VMDK)
* **Network:** Virtual NIC attached

---

### 🔹 VM Storage Types

* Dynamically allocated disk
* Fixed-size disk

---

## 🌐 **B. Virtual Machine Network Configuration**

### 🔹 Purpose of VM Networking

* Enable:

  * Internet access
  * VM-to-VM communication
  * VM-to-host communication
  * VM-to-external network communication

---

## 🔌 **C. VM Network Modes (Very Important for MCQs)**

### 🔹 1. NAT (Network Address Translation)

* VM accesses external network using host IP.
* VM **cannot be accessed directly** from outside.

**Use Case:** Internet access only.

📌 **Key Point:**

* Default mode in VirtualBox

---

### 🔹 2. Bridged Adapter

* VM gets IP from **same network as host**.
* VM behaves like a **physical machine**.

**Use Case:** Server setup, LDAP, Apache, NIS labs.

📌 **Key Point:**

* VM is accessible from LAN.

---

### 🔹 3. Host-Only Adapter

* Communication only between **Host ↔ VM**.
* No internet access.

**Use Case:** Secure testing, internal labs.

---

### 🔹 4. Internal Network

* Communication only between **VMs**.
* Host not accessible.

**Use Case:** Isolated VM clusters.

---

### 🔹 5. Not Attached

* VM has no network connectivity.

---

## 📊 **4. Important Facts / Points for MCQs**

* Hypervisor manages **hardware abstraction**
* VirtualBox is a **Type-2 hypervisor**
* NAT is **most secure but least accessible**
* Bridged networking gives **real LAN IP**
* Host-only network has **no internet**
* One VM can have **multiple network adapters**
* VM NIC behaves like **eth0 / ens33**

---

## 💡 **5. Examples**

* Apache cluster VMs use **Bridged Adapter**
* LDAP/NIS server VM requires **static IP**
* Practice labs use **Host-only + NAT (dual NIC)**

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* NAT ≠ Bridged
* Host-only ≠ Internal Network
* Hypervisor ≠ Guest OS
* VM IP in NAT is **private**
* Bridged mode depends on **physical NIC**
* Snapshot ≠ Backup
* VM shutdown ≠ Host shutdown

---

📌 **Quick Revision Formula for Exams:**

* **NAT → Internet only**
* **Bridged → LAN + Internet**
* **Host-only → Host ↔ VM**
* **Internal → VM ↔ VM**
