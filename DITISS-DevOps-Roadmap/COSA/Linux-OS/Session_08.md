## 💽🗄️ **Session 8 – Disk Management (PG-DITISS)**

---

## 🔹 **1. Concept Overview**

Session 8 covers **Linux disk management**, a **high-weight lab + MCQ topic**:

* Disk & partition concepts
* Partitioning tools: **fdisk, gdisk**
* **LVM (Logical Volume Manager)**
* **Lab:** Disk partitioning and LVM operations

> Content strictly aligned with **COSA-Linux.pdf** (Disk Management section) and PG-DITISS exam focus.

---

## 📘 **2. Key Definitions**

* **Disk:** Physical storage device (HDD/SSD).
* **Partition:** Logical division of a disk.
* **Filesystem:** Structure used to store/manage files (ext4, xfs).
* **MBR:** Master Boot Record (legacy partition table).
* **GPT:** GUID Partition Table (modern partition table).
* **LVM:** Logical Volume Manager – flexible disk management layer.
* **PV:** Physical Volume (LVM disk/partition).
* **VG:** Volume Group (pool of storage).
* **LV:** Logical Volume (usable logical partition).

---

## 🧩 **3. Main Content (Organized from COSA Notes)**

---

### 💾 **A. Disk & Partition Basics**

* Linux treats disks as files:

  * `/dev/sda`, `/dev/sdb`
* Partitions:

  * `/dev/sda1`, `/dev/sda2`

**Disk Types:**

* HDD, SSD
* Primary, Extended, Logical partitions

**Exam One-liner:**
👉 *Everything in Linux is a file – including disks.*

---

### 🧱 **B. Partition Tables (MCQ Favorite)**

| Feature         | MBR       | GPT    |
| --------------- | --------- | ------ |
| Max partitions  | 4 primary | 128    |
| Disk size limit | 2 TB      | > 2 TB |
| Tool            | fdisk     | gdisk  |
| Modern support  | ❌         | ✅      |

---

### 🛠️ **C. fdisk – Disk Partitioning Tool**

(from COSA)

* Used for **MBR partitioning**
* Works on disks ≤ 2 TB
* Interactive CLI tool

**Common fdisk Commands:**

| Key | Function              |
| --- | --------------------- |
| `n` | New partition         |
| `d` | Delete partition      |
| `p` | Print partition table |
| `w` | Write changes         |
| `q` | Quit without saving   |

**Command:**

```bash
fdisk /dev/sdb
```

---

### 🧰 **D. gdisk – GPT Disk Partitioning**

* Used for **GPT partition tables**
* Supports large disks
* Similar interface to fdisk

**Command:**

```bash
gdisk /dev/sdb
```

**Exam Point:**
👉 *gdisk = GPT, fdisk = MBR*

---

### 🧩 **E. Logical Volume Manager (LVM)**

LVM adds a **logical layer** between disk and filesystem.

#### 🔹 LVM Components

1. **Physical Volume (PV)**

   * Disk/partition used by LVM
   * Example: `/dev/sdb1`

2. **Volume Group (VG)**

   * Pool of storage created from PVs

3. **Logical Volume (LV)**

   * Acts like a partition
   * Mounted & formatted

---

#### 🔹 LVM Workflow (Exam Flowchart)

1. Create PV
2. Create VG
3. Create LV
4. Format LV
5. Mount LV

---

#### 🔹 Important LVM Commands

| Command     | Purpose           |
| ----------- | ----------------- |
| `pvcreate`  | Create PV         |
| `vgcreate`  | Create VG         |
| `lvcreate`  | Create LV         |
| `pvdisplay` | Show PV info      |
| `vgdisplay` | Show VG info      |
| `lvdisplay` | Show LV info      |
| `lvextend`  | Extend LV         |
| `resize2fs` | Resize filesystem |

---

### ⭐ **Advantages of LVM (MCQ-Oriented)**

* Dynamic resizing
* No downtime required
* Multiple disks treated as one
* Easy disk expansion

---

## 📌 **4. Important Facts / Points for MCQs**

* fdisk → MBR only
* gdisk → GPT only
* GPT supports > 2 TB disks
* LVM = flexible disk management
* LV behaves like normal partition
* PV → VG → LV (order matters)

---

## 🧪 **5. Examples**

* Create partition:

  ```bash
  fdisk /dev/sdb
  ```
* Create LVM:

  ```bash
  pvcreate /dev/sdb1
  vgcreate vgdata /dev/sdb1
  lvcreate -L 5G -n lvdata vgdata
  mkfs.ext4 /dev/vgdata/lvdata
  mount /dev/vgdata/lvdata /mnt
  ```

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* ❌ fdisk cannot handle >2 TB disks
* ❌ LVM is NOT a filesystem
* ⚠️ GPT ≠ filesystem
* ⚠️ LV name ≠ mount point
* ⚠️ pvcreate works on **partition or disk**

---
