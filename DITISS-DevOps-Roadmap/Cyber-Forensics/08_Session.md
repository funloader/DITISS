# SESSION 8 – COMPUTER FORENSICS TOOLS

---

## **1. Computer Forensics Tools – Overview**

### **Concept Overview**

* **Computer forensics tools** are specialized software used to **identify, acquire, preserve, analyze, and report digital evidence**.
* Tool selection depends on:

  * OS
  * Evidence type
  * Stage of investigation

📌 **MCQ Trap**

* Tools must be **forensically sound** and **court-acceptable**

---

## **2. Sysinternals Suite**

### **Definition**

* A collection of **Windows system utilities** developed by **Microsoft Sysinternals**.

---

### **Purpose**

* **Live system analysis**
* Troubleshooting and incident response

---

### **Key Sysinternals Tools (Exam-Relevant)**

| Tool             | Function                         |
| ---------------- | -------------------------------- |
| Process Explorer | View running processes           |
| Process Monitor  | File, registry, process activity |
| Autoruns         | Startup programs                 |
| TCPView          | Network connections              |
| PsTools          | Remote system management         |
| RAMMap           | Memory usage                     |
| Sigcheck         | File signature verification      |

---

### **Forensic Use**

* Volatile data collection
* Malware investigation
* Live response analysis

📌 **MCQ Trap**

* Sysinternals ≠ forensic imaging tool
* Used on **live systems**

---

## **3. FTK (Forensic Toolkit)**

### **Definition**

* **Commercial digital forensics software** developed by **AccessData**.

---

### **Key Capabilities**

* Disk & file system analysis
* Data indexing
* Keyword searching
* Email analysis
* Registry analysis
* Malware detection
* Reporting

---

### **Forensic Role**

* Evidence examination & analysis

📌 **MCQ Trap**

* FTK ≠ FTK Imager

---

## **4. FTK Imager**

### **Definition**

* A **lightweight forensic acquisition tool** by AccessData.

---

### **Key Features**

* Create forensic images
* Preview files
* Capture volatile memory
* Verify hashes
* Mount images read-only

---

### **Supported Formats**

* RAW (dd)
* E01
* AFF

📌 **MCQ Trap**

* FTK Imager is mainly for **acquisition**, not deep analysis

---

## **5. OSF (Open Source Forensics)**

### **Definition**

* Collection of **open-source digital forensic tools**.

---

### **Key Characteristics**

* Free to use
* Community supported
* Transparent algorithms

---

### **Examples**

* Autopsy
* Sleuth Kit
* Volatility
* Plaso

---

### **Advantages**

* Cost-effective
* Customizable

---

### **Limitations**

* Limited official support
* Requires expertise

📌 **MCQ Trap**

* Open source ≠ unreliable
* Courts accept OSF if methodology is sound

---

## **6. Hex (Hex Editor Tools)**

### **Definition**

* Tools used to **view and edit data at hexadecimal (byte) level**.

---

### **Common Hex Editors**

* HxD
* WinHex
* Hex Workshop

---

### **Forensic Uses**

* File header/footer analysis
* Detect file type mismatch
* Analyze raw disk data
* Malware reverse engineering

📌 **MCQ Trap**

* Hex editors work at **byte level**, not logical file level

---

## **Important Facts / Points for MCQs**

* Sysinternals → live Windows analysis
* FTK → full forensic analysis
* FTK Imager → acquisition tool
* OSF → open-source forensic tools
* Hex editor → raw data analysis

---

## **MCQ Pointers / Exam Traps**

* FTK vs FTK Imager
* Sysinternals vs Hex editor
* Open source vs commercial tools
* Acquisition vs analysis tools
* Live response vs post-mortem analysis

---

## **Corrections / Improvements / Suggested Substitutions**

1. **Terminology**

   * Use *“FTK (Forensic Toolkit)”*, not *Forensics Tool kit*
2. **Clarification**

   * Sysinternals tools are **not forensic-imaging tools**
3. **Exam Focus**

   * Tool purpose is frequently asked, not commands
4. **Best Practice**

   * Always validate tool output with hashing
