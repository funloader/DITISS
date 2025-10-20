# 💾 Storage Area Network (SAN) — Session 9

**Duration:** 2 Theory Hours + Lab Assignment
**Module:** DevOps (CDAC PG-DITISS)
**Objective:** To understand the concepts of Storage Area Networks (SANs), their role in high availability, and practical implementation using open-source tools like FreeNAS (TrueNAS CORE).

---

## 📘 **Theory Checklist**

### 🧩 Introduction to Storage Area Networks (SAN)
- [x] Understand the purpose and architecture of a **Storage Area Network (SAN)**.
- [x] Differentiate between SAN, NAS, and Direct Attached Storage (DAS).
- [x] Learn the role of SAN in large-scale IT infrastructure.

---

### 🧱 SAN Configuration and High Availability
- [x] Review methods for **Configuring a SAN** (e.g., using FreeNAS).
- [x] Study techniques for **Using SAN for high availability** (HA).
- [x] Understand **Multipath I/O (MPIO)** and its function in ensuring redundancy and performance.

---

### 🗄️ Storage Technologies
- [x] Learn about **ZFS Volume Configuration** and its features (data integrity, snapshots).
- [x] Explore **IP-Based Storage Communication** protocols (iSCSI, NFS, CIFS/SMB).
- [x] Introduction to **Object Storage services** and their use cases (e.g., MinIO).

---

## 🧪 **Lab Assignments**

### 1. FreeNAS (TrueNAS CORE) Installation and Basic Setup
- [x] Download and install FreeNAS (TrueNAS CORE) in a virtual machine (using VirtualBox/VMware Workstation).
- [x] Configure a **storage pool** and create a **ZFS dataset** to be used as a SAN.

---

### 2. High Availability with iSCSI and MPIO
- [x] Set up **two instances of FreeNAS** in virtual machines.
- [x] Configure **iSCSI targets** on both instances.
- [x] Set up **multipath I/O (MPIO)** on the host machine to simulate high availability.

---

### 3. ZFS Volume Management and Features
- [x] Within the FreeNAS VM, create a **ZFS pool** using multiple virtual disks.
- [x] Add datasets, and configure **snapshots and replication**.
- [x] Use the FreeNAS web interface to manage the ZFS volumes.

---

### 4. File and Object Storage Configuration
- [x] Configure **NFS and CIFS/SMB shares** on the FreeNAS virtual machine.
- [x] Use a host PC to connect to these shares, map network drives, and transfer files.
- [x] Install **MinIO** (open-source object storage server) within a virtual machine.
- [x] Set up a bucket, upload objects, and configure access policies using the MinIO interface/CLI.

---

## 🧰 **Tools & Platforms**
- 🖥️ **FreeNAS** (TrueNAS CORE)
- 💾 **iSCSI**
- ☁️ **MinIO** (Object Storage)
- 🌐 **VirtualBox / VMware Workstation**
- 🗄️ **ZFS**

---

## 🎯 **Learning Outcomes**
By completing this session, you will:
- ✅ Be able to deploy and configure a software-defined SAN using FreeNAS/TrueNAS.
- ✅ Understand and implement redundant storage paths using iSCSI and MPIO.
- ✅ Utilize ZFS features like snapshots for data protection and replication.
- ✅ Differentiate and configure file (NFS, CIFS) and object storage (MinIO) services.

---
