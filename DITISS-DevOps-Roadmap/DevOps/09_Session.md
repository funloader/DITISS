## 📘 **Session 9: Storage Area Network (SAN) & Advanced Storage Concepts**

---

### 🧠 **1. Concept Overview**

* **Storage Area Network (SAN)** is a **dedicated, high-speed network** that provides **block-level storage** to servers.
* SAN separates **storage from compute**, improving **performance, scalability, and availability**.
* Commonly used in **enterprise data centers**, virtualization, and HA environments.

---

### 📖 **2. Key Definitions**

* **SAN (Storage Area Network):** A specialized network that connects servers to shared storage devices using **block-level access**.
* **Block Storage:** Data stored in fixed-sized blocks (used by SAN).
* **FreeNAS:** An **open-source storage OS** used to configure SAN/NAS services.
* **ZFS:** Advanced file system with **volume management + data protection**.
* **High Availability (HA):** System design ensuring **minimal downtime**.

---

### 🧩 **3. Main Content (Organized from Notes)**

---

#### 🗄️ **Storage Area Network (SAN)**

* Provides **shared storage pool** to multiple servers.
* Used for:

  * Databases
  * Virtual machines
  * Backup & disaster recovery
* Operates independently of **LAN**.

**SAN Components:**

* Hosts (Servers)
* Storage devices (Disk arrays, tape libraries)
* SAN switches
* High-speed interconnects

---

#### ⚙️ **Advantages of SAN**

* High scalability
* Better disk utilization
* High security
* Easy addition/removal of storage devices
* Improved performance
* Suitable for mission-critical applications

---

#### 🛠️ **Configuring a SAN (FreeNAS)**

* **FreeNAS** is used to configure and manage SAN storage.
* Supports:

  * iSCSI (block storage)
  * ZFS volumes
* Steps (Conceptual – Exam Focus):

  * Install FreeNAS
  * Configure storage disks
  * Create ZFS pool
  * Configure iSCSI target
  * Connect client systems

📌 *FreeNAS is commonly used in labs and learning environments.*

---

#### 🔁 **Using SAN for High Availability**

* SAN enables **shared storage** between clustered servers.
* If one server fails:

  * Another server accesses the **same data**
* Key role in:

  * Failover clustering
  * Business continuity

**Why SAN supports HA?**

* Centralized storage
* No local disk dependency
* Faster recovery

---

#### 🧮 **ZFS Volume Configuration**

* **ZFS (Zettabyte File System)** combines:

  * File system
  * Logical volume manager
* Features:

  * Data integrity checks
  * Snapshots
  * Cloning
  * RAID support

**ZFS Concepts:**

* **Zpool:** Collection of physical disks
* **Dataset:** File system inside a pool
* **Zvol:** Block device used for SAN (iSCSI)

---

#### 🌐 **IP-Based Storage Communication**

* Uses **standard IP networks** for storage access.
* Common protocol:

  * **iSCSI (Internet Small Computer System Interface)**

**Features:**

* Block-level storage over TCP/IP
* Cheaper than Fibre Channel
* Uses Ethernet infrastructure

---

#### 📦 **Object Storage Services**

* Stores data as **objects** instead of blocks or files.
* Each object includes:

  * Data
  * Metadata
  * Unique ID

**Characteristics:**

* Highly scalable
* Used in cloud environments
* Suitable for unstructured data

**Examples:**

* Amazon S3
* OpenStack Swift

---

### 🎯 **4. Important Facts / Points for MCQs**

* SAN uses **block-level storage**
* FreeNAS supports **iSCSI + ZFS**
* ZFS provides **snapshots and cloning**
* iSCSI works over **IP networks**
* Object storage ≠ SAN storage
* SAN is ideal for **HA clusters**

---

### 🧪 **5. Examples**

* SAN + Cluster → High availability
* FreeNAS + iSCSI → SAN implementation
* ZFS snapshot → Quick rollback
* Amazon S3 → Object storage

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* **SAN vs NAS** (Block vs File storage)
* **iSCSI vs Fibre Channel**
* ZFS ≠ RAID (ZFS manages RAID internally)
* Object storage ≠ block storage
* FreeNAS ≠ Cloud storage
* SAN improves availability, **not application logic**

---

✅ **Exam Tip:**

> *Expect MCQs on SAN vs NAS, ZFS features, iSCSI protocol, and HA usage scenarios.*
