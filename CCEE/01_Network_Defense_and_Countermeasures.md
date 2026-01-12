> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 01

---

### 1. In a corporate network, an administrator notices unusual traffic patterns but no immediate system failures. What is the **primary function of an Intrusion Detection System (IDS)** in this scenario?

* [ ] Preventing network attacks
* [ ] Detecting and alerting on network or system intrusions
* [ ] Blocking unauthorized access to the system
* [ ] Encrypting data during transmission

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Detecting and alerting on network or system intrusions
💡 IDS is designed to monitor systems and networks for suspicious activity and generate alerts. Unlike IPS, it does not actively block attacks. Reference: NIST SP 800-94.

</details>

---

### 2. Which characteristic differentiates an Intrusion Prevention System (IPS) from an IDS?

* [ ] It only detects intrusions and does not take action.
* [ ] It monitors and alerts on suspicious network traffic.
* [ ] It can automatically block malicious traffic in real-time.
* [ ] It is only used in cloud environments.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It can automatically block malicious traffic in real-time
💡 IPS extends IDS functionality by actively preventing attacks in addition to detecting them.

</details>

---

### 3. A network security engineer configures an IPS to respond to detected SQL injection attacks by immediately dropping suspicious packets. Which type of response is this?

* [ ] Generating an alert
* [ ] Logging suspicious activity
* [ ] Blocking malicious traffic
* [ ] Encrypting communication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Blocking malicious traffic
💡 Reactive IPS responses involve immediate actions to stop attacks, such as dropping or blocking malicious traffic.

</details>

---

### 4. Anomaly-based IDS relies on baseline modeling of normal network behavior. Which statement accurately describes its characteristics?

* [ ] It models the normal usage of network as a noise characterization
* [ ] It doesn’t detect novel attacks
* [ ] Anything distinct from the noise is not assumed to be intrusion activity
* [ ] It detects based on signature

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It models the normal usage of network as a noise characterization
💡 Anomaly-based IDS detects deviations from established normal behavior, enabling detection of unknown or zero-day attacks.

</details>

---

### 5. To detect **zero-day attacks** in a network, which IDS type is most suitable?

* [ ] Signature-based IDS
* [ ] Anomaly-based IDS
* [ ] Host-based IDS
* [ ] Network-based IDS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Anomaly-based IDS
💡 Signature-based systems rely on known attack patterns, whereas anomaly-based IDS can identify novel attacks by detecting deviations from normal behavior.

</details>

---

### 6. Which mechanism does an IDS primarily use to detect **known attack patterns**?

* [ ] Data packet inspection
* [ ] Heuristic algorithms
* [ ] Signatures
* [ ] Traffic volume analysis

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Signatures
💡 Signature-based IDS compares traffic or system behavior against a database of known attack patterns to identify threats.

</details>

---

### 7. What is a key feature of a **host-based IDS (HIDS)**?

* [ ] It monitors network traffic between systems.
* [ ] It is installed on the network perimeter.
* [ ] It is typically used for enterprise-wide monitoring.
* [ ] It is installed on individual hosts or devices to detect attacks.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It is installed on individual hosts or devices to detect attacks
💡 HIDS monitors the internal activity of a host, including system calls, file access, and logins, providing granular protection.

</details>

---

### 8. Which type of IDS is most appropriate for monitoring and protecting a **critical application server**?

* [ ] Signature-based IDS
* [ ] Host-based IDS
* [ ] Network-based IDS
* [ ] Anomaly-based IDS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Host-based IDS
💡 HIDS provides direct protection on specific hosts by monitoring local activity, ideal for critical servers.

</details>

---

### 9. Which of the following is **not** a method used by IPS to prevent intrusions?

* [ ] Stateful packet inspection
* [ ] Traffic analysis and filtering
* [ ] Real-time traffic blocking
* [ ] User authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** User authentication
💡 IPS focuses on analyzing, detecting, and preventing malicious traffic, not performing user authentication.

</details>

---

### 10. A **hybrid IDS/IPS** combines multiple detection techniques. What is its primary advantage?

* [ ] The ability to detect only known threats
* [ ] The ability to combine both signature and anomaly-based detection techniques
* [ ] The ability to scan encrypted traffic
* [ ] The ability to block all traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The ability to combine both signature and anomaly-based detection techniques
💡 Hybrid systems leverage the strengths of multiple detection methods, improving coverage and detection accuracy.

</details>

---

### 11. When an IDS detects suspicious activity, it typically generates:

* [ ] A warning or alert
* [ ] A packet drop
* [ ] A system shutdown
* [ ] A patch for the system

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A warning or alert
💡 IDS alerts administrators to potential threats, enabling investigation and response without disrupting normal operations.

</details>

---

### 12. What is the **primary function of an IPS** in a network security architecture?

* [ ] Detecting attacks and blocking malicious traffic in real-time
* [ ] Encrypting network data
* [ ] Scanning email attachments for viruses
* [ ] Logging network traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Detecting attacks and blocking malicious traffic in real-time
💡 IPS actively prevents intrusions by stopping attacks as they occur, unlike IDS which is passive.

</details>

---

### 13. Which statement best differentiates an IDS from an IPS?

* [ ] An IDS can block traffic, while an IPS cannot.
* [ ] An IPS is deployed outside the network, while an IDS is deployed inside.
* [ ] An IPS can block malicious traffic, while an IDS only detects and alerts.
* [ ] An IDS is more secure than an IPS.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** An IPS can block malicious traffic, while an IDS only detects and alerts
💡 IDS is passive, while IPS is active in preventing attacks.

</details>

---

### 14. Which of the following is **not** a common IPS technique?

* [ ] Signature-based detection
* [ ] Anomaly-based detection
* [ ] Traffic encryption
* [ ] Stateful packet inspection

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Traffic encryption
💡 IPS techniques involve traffic analysis and control, not encrypting network traffic.

</details>

---

### 15. Upon detecting malicious traffic, what is the typical action of an IPS?

* [ ] Logs the event and sends an alert to administrators
* [ ] Encrypts the traffic for further analysis
* [ ] Blocks the malicious traffic and stops it from reaching its destination
* [ ] Redirects the traffic to a different network

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Blocks the malicious traffic and stops it from reaching its destination
💡 IPS actively prevents attacks in real-time, unlike IDS which only alerts.

</details>

---

### 16. What is the main advantage of a **network-based IPS (NIPS)**?

* [ ] It operates on a single host for real-time detection
* [ ] It monitors the entire network traffic in real-time
* [ ] It provides detailed reports for each host
* [ ] It automatically applies patches to the system

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It monitors the entire network traffic in real-time
💡 NIPS is deployed on network segments to provide holistic, real-time monitoring of traffic flows.

</details>

---

### 17. Which type of attack is most likely to be **detected and blocked** by an IPS?

* [ ] Zero-day attacks
* [ ] SQL injection attacks
* [ ] Brute force login attempts
* [ ] Social engineering attacks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SQL injection attacks
💡 IPS can inspect traffic payloads and patterns to prevent known attacks like SQL injection; social engineering cannot be blocked at network level.

</details>

---

### 18. Which of the following is an example of a **reactive response** by an IPS?

* [ ] Blocking a suspicious IP address
* [ ] Generating a warning alert
* [ ] Logging attack details
* [ ] Creating a backup of network data

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Blocking a suspicious IP address
💡 Reactive actions involve immediate intervention to stop or mitigate detected attacks.

</details>

---

### 19. The **primary purpose of an IPS** in a security architecture is:

* [ ] To encrypt data during transmission
* [ ] To identify and block potential threats in real-time
* [ ] To monitor the network for vulnerabilities
* [ ] To generate logs for auditing purposes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To identify and block potential threats in real-time
💡 IPS provides active defense by preventing attacks before they impact systems.

</details>

---

### 20. Which type of IPS inspects traffic against a set of **predefined rules and known attack patterns**?

* [ ] Behavior-based IPS
* [ ] Anomaly-based IPS
* [ ] Signature-based IPS
* [ ] Heuristic-based IPS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Signature-based IPS
💡 Signature-based IPS matches traffic against known patterns, effectively blocking known threats.

</details>

---

Perfect! I will continue the **CCEE-level enhancement** and numbering from the previous set (we ended at 20). I will revise these firewall MCQs to make them **scenario-based, single correct answer, and PG-DITISS exam appropriate**, with plausible distractors and explanations.

---

### 21. What is the **primary purpose of a firewall** in a network security setup?

* [ ] To store website data
* [ ] To block spam emails
* [ ] To filter incoming and outgoing network traffic
* [ ] To optimize CPU performance

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To filter incoming and outgoing network traffic
💡 Firewalls act as a barrier between trusted and untrusted networks, controlling traffic based on security rules.

</details>

---

### 22. Which of the following is a **recognized type of firewall**?

* [ ] Proxy firewall
* [ ] SSD firewall
* [ ] USB firewall
* [ ] DNS firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Proxy firewall
💡 Proxy firewalls operate at the application layer, acting as intermediaries between clients and servers.

</details>

---

### 23. Which firewall primarily operates at the **network layer (Layer 3) of the OSI model**?

* [ ] Packet-filtering firewall
* [ ] Application-layer firewall
* [ ] Stateful inspection firewall
* [ ] Next-Generation Firewall (NGFW)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Packet-filtering firewall
💡 Packet-filtering firewalls inspect source/destination IP addresses, ports, and protocol headers without examining payload content.

</details>

---

### 24. A **stateful firewall** can track which of the following?

* [ ] Only source IP
* [ ] The state of active connections
* [ ] File sizes
* [ ] Encryption algorithms

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The state of active connections
💡 Stateful firewalls maintain a session table to track connection states, allowing dynamic filtering based on connection context.

</details>

---

### 25. Which of the following is **not typically filtered by a firewall**?

* [ ] IP addresses
* [ ] Port numbers
* [ ] MAC addresses
* [ ] CPU temperature

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CPU temperature
💡 Firewalls filter traffic based on network-level information (IP, ports, protocols) and sometimes MAC addresses, but not hardware metrics like CPU temperature.

</details>

---

### 26. What is a major **disadvantage of a basic packet-filtering firewall**?

* [ ] It cannot block traffic
* [ ] It uses too much memory
* [ ] It doesn’t examine packet content
* [ ] It encrypts data by default

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It doesn’t examine packet content
💡 Packet-filtering firewalls are limited to header inspection and cannot detect application-layer attacks embedded in payloads.

</details>

---

### 27. When a firewall rule does not explicitly match a packet, what is the **default policy** followed by most secure firewalls?

* [ ] Allow
* [ ] Deny
* [ ] Ask
* [ ] Retry

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deny
💡 Secure firewalls follow a "default deny" policy to prevent unauthorized access unless explicitly permitted.

</details>

---

### 28. Which Linux command is commonly used to **configure firewall rules**?

* [ ] ifconfig
* [ ] netstat
* [ ] iptables
* [ ] traceroute

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** iptables
💡 iptables is the standard tool for configuring packet-filtering and NAT rules on Linux-based systems.

</details>

---

### 29. Which firewall type combines **packet filtering, stateful inspection, and deep packet inspection (DPI)**?

* [ ] Basic router
* [ ] Next-Generation Firewall (NGFW)
* [ ] Transparent proxy
* [ ] Wi-Fi repeater

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Next-Generation Firewall (NGFW)
💡 NGFWs integrate multiple security functions, including DPI, intrusion prevention, and application awareness.

</details>

---

### 30. In firewall terminology, what does **DMZ (Demilitarized Zone)** refer to?

* [ ] A zone free from any firewall control
* [ ] An area only accessible to administrators
* [ ] A subnet that separates internal networks from external traffic
* [ ] A wireless network

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A subnet that separates internal networks from external traffic
💡 The DMZ hosts publicly accessible services (e.g., web servers) while protecting the internal network from direct external access.

</details>

---

### 31. In a stateful firewall, which component tracks **connection context over time**?

* [ ] Rule-based policy table
* [ ] NAT table
* [ ] Session table (state table)
* [ ] Access control list (ACL)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Session table (state table)
💡 The session table stores information about active connections, enabling stateful inspection of network traffic.

</details>

---

### 32. Which attack technique is most effective at **evading stateless packet-filtering firewalls**?

* [ ] IP spoofing
* [ ] TCP SYN flood
* [ ] Fragmentation attacks
* [ ] Brute force

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fragmentation attacks
💡 Stateless firewalls inspect packets individually; fragmented packets can bypass simple filters because the full context is missing.

</details>

---

### 33. Regarding **Deep Packet Inspection (DPI)** in NGFWs, which statement is correct?

* [ ] It only inspects TCP headers
* [ ] It is limited to Layer 3 and Layer 4
* [ ] It analyzes the payload and application behavior
* [ ] It cannot detect encrypted threats

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It analyzes the payload and application behavior
💡 DPI examines the content of packets, enabling detection of application-layer attacks and malware.

</details>

---

### 34. In a corporate firewall deployment, where is the **DMZ typically placed**?

* [ ] Between two internal LAN segments
* [ ] Between the internet and the external router
* [ ] Between the internal network and the external (untrusted) network
* [ ] Between VLANs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Between the internal network and the external (untrusted) network
💡 Placing the DMZ between internal and external networks protects internal resources while providing controlled public access.

</details>

---

### 35. Which firewall type is most effective against **application-layer (Layer 7) attacks**?

* [ ] Packet-filtering firewall
* [ ] Proxy-based firewall
* [ ] Circuit-level gateway
* [ ] Stateless NAT firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Proxy-based firewall
💡 Proxy firewalls operate at the application layer and can inspect and filter specific application protocols (e.g., HTTP, FTP).

</details>

---

### 36. What is a potential drawback of using a **transparent firewall** in a network?

* [ ] It does not support NAT
* [ ] It requires static IPs
* [ ] It cannot perform deep packet inspection
* [ ] It is not visible to attackers and can be bypassed easily

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It does not support NAT
💡 Transparent firewalls are deployed at Layer 2 and act like a bridge; they typically cannot perform NAT operations.

</details>

---

### 37. Which protocol inspection can prevent **FTP bounce attacks** in firewalls?

* [ ] ICMP inspection
* [ ] Stateful TCP inspection
* [ ] Deep packet inspection of FTP control channel
* [ ] DNS cache filtering

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deep packet inspection of FTP control channel
💡 DPI allows the firewall to monitor FTP commands and prevent malicious port redirection attempts.

</details>

---

### 38. Which firewall rule set is considered **most secure by default**?

* [ ] Allow all inbound and outbound
* [ ] Deny inbound, allow outbound
* [ ] Allow inbound if requested
* [ ] Deny all inbound and outbound unless explicitly allowed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deny all inbound and outbound unless explicitly allowed
💡 "Default deny" minimizes attack surface by allowing only explicitly authorized traffic.

</details>

---

### 39. What is the key difference between **circuit-level gateways** and **application-layer firewalls**?

* [ ] Circuit-level gateways operate at Layer 3
* [ ] Application-layer firewalls do not inspect content
* [ ] Circuit-level gateways monitor TCP handshakes but not data
* [ ] Application-layer firewalls cannot log traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Circuit-level gateways monitor TCP handshakes but not data
💡 Circuit-level gateways ensure session integrity but cannot inspect application payloads, unlike application-layer firewalls.

</details>

---

### 40. What is a **firewall used for** in computer networks?

* [ ] To install antivirus
* [ ] To block unauthorized access
* [ ] To format the hard drive
* [ ] To increase internet speed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To block unauthorized access
💡 Firewalls control network traffic to prevent unauthorized access, acting as a key perimeter defense mechanism.

</details>

---

