# 🔐 Security Concepts — PG-DITISS August 2025

**Duration:** 50 Classroom Hours + 60 Lab Hours  
**Total:** 110 Hours  
**Module:** Security Concepts (Application Security, Ethical Hacking, and Mobile Security)  
**Objective:**  
To provide comprehensive understanding and practical exposure in application security, ethical hacking, and mobile security.  
This module focuses on identifying, exploiting, and mitigating vulnerabilities in systems, applications, and mobile environments.

---

## 🧩 **Application Security (Sessions 1–5)**

### 🧠 **Session 01: OWASP Top 10 — Web Application Vulnerabilities**
- [ ] Understand the **OWASP Top 10** list of web application vulnerabilities.  
- [ ] Study the importance of web application testing and secure coding practices.  
- [ ] Learn about input validation, authentication, and session management flaws.  

**🧪 Lab:**  
- Perform **Web Vulnerability Testing** using **OWASP ZAP** and **Burp Suite**.  
- Identify and analyze vulnerabilities in a sample PHP or Python-based web app.  

---

### 🧠 **Session 02: Denial of Service (DoS) and Buffer Overflow Attacks**
- [ ] Understand **DoS/DDoS** attack mechanisms and their impact.  
- [ ] Learn about **Buffer Overflow Attacks**, memory corruption, and exploitation.  

**🧪 Lab:**  
- Simulate a DoS attack using **Hping3** or **LOIC** (in controlled lab).  
- Demonstrate a simple **buffer overflow** using vulnerable C code in a sandbox.  

---

### 🧠 **Session 03: Cryptography and Web Security**
- [ ] Study the fundamentals of **Cryptography** (Symmetric & Asymmetric).  
- [ ] Explore **SSL/TLS**, hashing, and certificate validation.  
- [ ] Understand how cryptography protects data transmission and authentication.  

**🧪 Lab:**  
- Generate **public/private key pairs** using **OpenSSL**.  
- Implement **HTTPS configuration** for a local web server.  

---

### 🧠 **Session 04: Secure Coding and Input Validation**
- [ ] Learn **secure coding practices** to mitigate injection and validation flaws.  
- [ ] Understand **SQL Injection**, **Cross-Site Scripting (XSS)**, and **Command Injection**.  

**🧪 Lab:**  
- Use **DVWA (Damn Vulnerable Web App)** to demonstrate SQLi and XSS exploits.  
- Apply input validation techniques to fix these vulnerabilities.  

---

### 🧠 **Session 05: Security Assessment and Reporting**
- [ ] Understand **vulnerability assessment** and **penetration testing reporting**.  
- [ ] Learn documentation best practices, remediation plans, and compliance requirements.  

**🧪 Lab:**  
- Create a **web application security assessment report**.  
- Include findings, exploited vulnerabilities, screenshots, and remediation steps.  

---

## 💻 **Ethical Hacking (Sessions 6–20)**

### 🧠 **Session 06: Introduction to Ethical Hacking**
- [ ] Understand **ethical hacking lifecycle** — Reconnaissance to Reporting.  
- [ ] Learn about **Hacker types**, legal considerations, and testing methodologies.  

**🧪 Lab:**  
- Perform **network reconnaissance** using **Nmap** and **Whois**.  

---

### 🧠 **Session 07: Footprinting and Reconnaissance**
- [ ] Study techniques for **Information Gathering** from public and private sources.  
- [ ] Learn about **DNS enumeration, Google Dorking**, and **Social Engineering**.  

**🧪 Lab:**  
- Conduct **active and passive footprinting** using **theHarvester**, **Maltego**, and **Recon-ng**.  

---

### 🧠 **Session 08: Scanning Networks**
- [ ] Understand **Network Scanning**, **Port Scanning**, and **Service Discovery**.  
- [ ] Identify live systems and open ports using automated tools.  

**🧪 Lab:**  
- Use **Nmap**, **Netcat**, and **Zenmap** for network and port scanning.  

---

### 🧠 **Session 09: Enumeration Techniques**
- [ ] Learn **SNMP, LDAP, NetBIOS**, and **SMTP enumeration**.  
- [ ] Understand how enumeration reveals sensitive information about systems.  

**🧪 Lab:**  
- Perform **SMB and SNMP enumeration** using **enum4linux** and **snmpwalk**.  

---

### 🧠 **Session 10: System Hacking and Privilege Escalation**
- [ ] Understand system hacking concepts — **Password Cracking**, **Privilege Escalation**, and **Rootkits**.  
- [ ] Study post-exploitation techniques and persistence methods.  

**🧪 Lab:**  
- Crack Windows passwords using **John the Ripper** and **Hydra**.  
- Demonstrate privilege escalation in a **Metasploitable2** environment.  

---

### 🧠 **Session 11: Malware Threats and Analysis**
- [ ] Study **Malware types** — Viruses, Worms, Trojans, Ransomware, Spyware.  
- [ ] Learn **Behavioral Analysis** and **Static/Dynamic Analysis** methods.  

**🧪 Lab:**  
- Analyze malware behavior using **ProcMon**, **Process Explorer**, and **VirusTotal**.  

---

### 🧠 **Session 12: Sniffing and Spoofing**
- [ ] Understand **Packet Sniffing**, **ARP Poisoning**, and **MAC Spoofing**.  
- [ ] Learn how attackers intercept and manipulate network traffic.  

**🧪 Lab:**  
- Use **Wireshark** and **Ettercap** to capture and analyze traffic.  
- Demonstrate ARP spoofing in a controlled environment.  

---

### 🧠 **Session 13: Social Engineering**
- [ ] Study psychological manipulation techniques used in **phishing**, **baiting**, and **pretexting**.  
- [ ] Learn how to design **phishing campaigns** for awareness.  

**🧪 Lab:**  
- Create a mock phishing email using **SET (Social Engineering Toolkit)**.  

---

### 🧠 **Session 14: Denial of Service and Session Hijacking**
- [ ] Understand **DoS/DDoS**, SYN floods, and session hijacking attacks.  
- [ ] Explore detection and mitigation techniques.  

**🧪 Lab:**  
- Simulate a **SYN flood** with **Hping3** and analyze logs.  
- Demonstrate **session hijacking** using **Burp Suite**.  

---

### 🧠 **Session 15: Web Server Hacking**
- [ ] Study web server vulnerabilities and misconfigurations.  
- [ ] Learn **directory traversal** and **web shell** exploitation.  

**🧪 Lab:**  
- Exploit vulnerable Apache/IIS server using **Metasploit** modules.  
- Harden the server against attacks.  

---

### 🧠 **Session 16: Wireless Network Hacking**
- [ ] Learn **WEP/WPA/WPA2** security mechanisms.  
- [ ] Understand **Wireless sniffing and cracking**.  

**🧪 Lab:**  
- Use **Aircrack-ng**, **airodump-ng**, and **aireplay-ng** to test wireless security.  

---

### 🧠 **Session 17: IDS, Firewalls, and Honeypots**
- [ ] Understand **IDS/IPS** operation and configuration.  
- [ ] Learn **Firewall policies**, **UTM**, and **Honeypot deployment**.  

**🧪 Lab:**  
- Configure **pfSense Firewall** and **Snort IDS** in a virtual lab.  

---

### 🧠 **Session 18: SQL Injection and Web Attacks**
- [ ] Study **SQL Injection**, **Command Injection**, and **Directory Traversal**.  
- [ ] Learn mitigation techniques.  

**🧪 Lab:**  
- Exploit **DVWA** and patch vulnerabilities using secure code.  

---

### 🧠 **Session 19: Vulnerability Analysis**
- [ ] Learn **Vulnerability Assessment Lifecycle**.  
- [ ] Understand **automated scanning tools and CVSS scoring**.  

**🧪 Lab:**  
- Perform a vulnerability scan using **OpenVAS** or **Nessus**.  

---

### 🧠 **Session 20: Report Writing and Remediation**
- [ ] Document test results, exploit details, and mitigation measures.  
- [ ] Learn professional report formats for audits and compliance.  

**🧪 Lab:**  
- Submit a full **ethical hacking report** based on lab exercises.  

---

## 📱 **Mobile Security (Sessions 21–25)**

### 🧠 **Session 21: Introduction to Mobile Security**
- [ ] Understand mobile platform architecture (Android/iOS).  
- [ ] Learn common mobile attack vectors and threats.  

**🧪 Lab:**  
- Analyze mobile app permissions and manifest files.  

---

### 🧠 **Session 22: Android App Security**
- [ ] Study Android app components, APK structure, and data storage.  
- [ ] Learn reverse engineering using **APKTool** and **JADX**.  

**🧪 Lab:**  
- Decompile and inspect an Android APK for vulnerabilities.  

---

### 🧠 **Session 23: iOS Security**
- [ ] Understand iOS security model and sandboxing.  
- [ ] Learn iOS app testing techniques.  

**🧪 Lab:**  
- Perform **static analysis** on iOS apps using **MobSF**.  

---

### 🧠 **Session 24: Mobile Application Penetration Testing**
- [ ] Study mobile app testing methodologies and tools.  
- [ ] Identify **Insecure Storage**, **Weak Authentication**, and **Data Leakage**.  

**🧪 Lab:**  
- Test vulnerable apps using **MobSF**, **QARK**, and **Drozer**.  

---

### 🧠 **Session 25: Mobile Security Reporting**
- [ ] Document mobile app vulnerabilities, exploit steps, and risk rating.  
- [ ] Suggest mitigation strategies and security best practices.  

**🧪 Lab:**  
- Prepare a **mobile security assessment report** with screenshots and fixes.  

---

## 🧰 **Tools & Platforms**

| Category | Tools |
|-----------|-------|
| 🌐 Web & App Security | OWASP ZAP, Burp Suite, Nikto, SQLMap, DVWA |
| 💻 Ethical Hacking | Kali Linux, Metasploit, Nmap, Netcat, Hydra |
| 🔒 Network Security | Snort, pfSense, Wireshark, Aircrack-ng |
| 🧩 Mobile Security | MobSF, Drozer, QARK, APKTool |
| 🧾 Reporting | Dradis, Faraday, Serpico |

---

## 🎯 **Learning Outcomes**
By completing this module, you will:
- ✅ Identify and exploit vulnerabilities in web and mobile applications.  
- ✅ Perform complete **ethical hacking cycles** — reconnaissance to reporting.  
- ✅ Analyze and defend against **network and wireless threats**.  
- ✅ Apply **secure coding and cryptographic principles**.  
- ✅ Conduct **vulnerability assessments** using industry-standard tools.  
- ✅ Create comprehensive **security audit and penetration test reports**.  

---

## ✍️ **Personal Notes**
> Use this section for your own commands, findings, and screenshots from each session.

```bash
# Common Commands
nmap -sV -p 1-1024 192.168.1.0/24
sqlmap -u "http://target.com/page.php?id=1" --dbs
apktool d vulnerable_app.apk
