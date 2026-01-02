# SESSION 9 – ACTIVE SYSTEMS, LINUX, AND MOBILE FORENSICS

---

## **1. Collecting and Analyzing Artefacts from Active Systems**

### **Concept**

* **Active system (live system) forensics**: Analyzing a system that is **powered on and running**.
* Focuses on **volatile data** (data lost on shutdown) and **real-time activity**.
* Complements traditional disk-based (static) forensics.

---

### **Types of Artefacts in Active Systems**

| Artefact                                  | Description                                        | Forensic Value                          |
| ----------------------------------------- | -------------------------------------------------- | --------------------------------------- |
| RAM / Memory                              | Current processes, loaded malware, encryption keys | Highly volatile, time-sensitive         |
| Network connections                       | Open connections, sockets, IPs                     | Detect intrusions, data exfiltration    |
| Running processes                         | Active applications, services                      | Detect malware, insider activity        |
| System logs                               | Security logs, event logs                          | Timeline reconstruction                 |
| Open files                                | Files in use by processes                          | Can indicate suspect activity           |
| Registry (Windows) / Config files (Linux) | System state, startup programs                     | System behavior, persistence mechanisms |

---

### **Collection Methods**

1. **Memory Imaging**

   * Tools: FTK Imager, Volatility, DumpIt
   * Captures **RAM snapshot**
2. **Network Monitoring**

   * Tools: Wireshark, TCPView
   * Logs **active connections** and traffic
3. **Process / Task Listing**

   * Commands: `tasklist`, `ps aux`, `top`
4. **System Logs**

   * Export event logs / syslog files

---

### **MCQ Tips**

* **Live vs Dead forensics**: Live = volatile data, Dead = disk only
* **Tools for memory capture** = FTK Imager, DumpIt
* **Don’t shut down system** before volatile data collection

---

## **2. Collecting and Analyzing Artefacts from Linux Systems**

### **Key Concepts**

* Linux artefacts differ from Windows:

  * File system: **Ext3/Ext4**
  * Logs: `/var/log/` (syslog, auth.log)
  * Config: `/etc/`, `/home/username/.bash_history`
  * Processes: `ps`, `top`, `lsof`
  * Network: `netstat`, `ss`, `iptables`

---

### **Key Linux Artefacts**

| Artefact           | Location / Command   | Forensic Use                 |
| ------------------ | -------------------- | ---------------------------- |
| User activity      | `~/.bash_history`    | Command history              |
| Logs               | `/var/log/`          | Track events, login attempts |
| Running processes  | `ps aux`             | Active programs, malware     |
| Open files         | `lsof`               | Detect file access           |
| Scheduled tasks    | `crontab -l`         | Persistence mechanisms       |
| Installed software | `dpkg -l`, `rpm -qa` | Identify installed tools     |

---

### **Collection Tools**

* Open-source: SleuthKit, Autopsy, Volatility
* Linux native commands: `dd`, `tar`, `scp`
* Memory capture: LiME (Linux Memory Extractor)

📌 **MCQ Trap**

* Linux artefacts can be hidden in unusual paths: `/tmp/`, `/var/tmp/`, hidden files (`.` prefix)
* Command history can be **edited/deleted**, check timestamps

---

## **3. Introduction to Mobile Forensics**

### **Definition**

* Mobile forensics: **Acquisition, preservation, and analysis of digital evidence** from mobile devices (smartphones, tablets, wearables).

---

### **Key Artefacts**

| Artefact            | Description                     | Use                    |
| ------------------- | ------------------------------- | ---------------------- |
| Call logs / SMS     | Incoming/outgoing communication | Track interactions     |
| Contacts / Calendar | Address book, events            | Link to suspects       |
| App data            | WhatsApp, Telegram, emails      | Communication evidence |
| Location            | GPS / Wi-Fi / Cell tower        | Track movement         |
| Media               | Photos, videos, audio           | Evidence collection    |
| Deleted data        | Recoverable via forensic tools  | Hidden evidence        |
| SIM / SD card       | External storage                | Extra artefacts        |

---

### **Acquisition Techniques**

1. **Logical Acquisition**

   * Extract user-accessible data
   * Tools: Cellebrite UFED, Oxygen Forensic
2. **Physical Acquisition**

   * Bit-by-bit image of entire storage
   * Tools: UFED Physical Analyzer
3. **Cloud Acquisition**

   * Data synced to cloud accounts (iCloud, Google Drive)
   * Legal and privacy compliance needed

---

### **Forensic Challenges**

* Device encryption
* Locked devices / passcodes
* Frequent OS updates
* Large app ecosystem

---

### **MCQ Tips**

* Mobile forensics tools: UFED, Oxygen, MOBILedit Forensic
* Cloud forensics requires **legal permission**
* Logical acquisition ≠ physical acquisition

---

### **Exam Notes – Quick Recall Table**

| Domain        | Key Artefacts                                   | Tools                             |
| ------------- | ----------------------------------------------- | --------------------------------- |
| Active System | RAM, Processes, Open files, Network             | FTK Imager, Volatility, Wireshark |
| Linux         | Logs, Bash history, Crontab, Installed packages | SleuthKit, Autopsy, LiME          |
| Mobile        | Call/SMS, App data, Location, Media             | UFED, Oxygen, MOBILedit           |

---
