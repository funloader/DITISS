> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 15 


## **Session 16: Concept of Network Policy Server (NPS)**

---

### 1. In an enterprise WLAN environment, Network Policy Server (NPS) is deployed to control user access. What is the **primary function** of NPS in such a setup?

* [ ] Manage Group Policy Objects (GPOs)
* [ ] Provide name resolution services
* [ ] Enforce network access and authorization policies
* [ ] Configure and manage mail routing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enforce network access and authorization policies
💡 NPS acts as a RADIUS server that evaluates authentication and authorization requests against defined network policies.

</details>

---

### 2. An administrator wants to install NPS as a centralized authentication service. On which operating system is NPS officially available as a server role?

* [ ] Windows 10
* [ ] Windows Server
* [ ] Ubuntu Linux
* [ ] macOS Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Windows Server
💡 NPS is included as part of the **Network Policy and Access Services** role in Windows Server editions.

</details>

---

### 3. When a wireless controller sends authentication requests to NPS, which protocol is primarily used for this communication?

* [ ] FTP
* [ ] RADIUS
* [ ] SMTP
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RADIUS
💡 NPS implements the RADIUS protocol for authentication, authorization, and accounting (AAA).

</details>

---

### 4. Which scenario best represents a **real-world use case** for deploying NPS?

* [ ] Automating disk cleanup tasks
* [ ] Assigning IP addresses dynamically
* [ ] Authenticating VPN users connecting remotely
* [ ] Encrypting sensitive files on servers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticating VPN users connecting remotely
💡 NPS is commonly used with VPN, Wi-Fi (802.1X), and remote access solutions for centralized authentication.

</details>

---

### 5. An administrator wants to configure and manage NPS using graphical tools. Which Windows component is required?

* [ ] PowerShell ISE
* [ ] Server Manager
* [ ] Task Scheduler
* [ ] Registry Editor

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server Manager
💡 NPS is installed and managed via Server Manager and the NPS MMC snap-in.

</details>

---

### 6. In a standard RADIUS deployment, what role does NPS typically perform?

* [ ] RADIUS Client
* [ ] RADIUS Proxy
* [ ] RADIUS Server
* [ ] DNS Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RADIUS Server
💡 NPS evaluates authentication requests and returns accept or reject responses to RADIUS clients.

</details>

---

### 7. Before configuring Network Policy Server, which server role must be installed?

* [ ] DHCP Server
* [ ] File and Storage Services
* [ ] Network Policy and Access Services
* [ ] Print and Document Services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Policy and Access Services
💡 NPS is a sub-role under the Network Policy and Access Services role.

</details>

---

### 8. Which set correctly represents the **core components** of Network Policy Server?

* [ ] DNS, DHCP, and FTP
* [ ] Connection request policies, network policies, and health policies
* [ ] Firewall rules, SNMP agents, and proxies
* [ ] Local security policies and registry entries

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Connection request policies, network policies, and health policies
💡 These components define how requests are processed, authenticated, authorized, and validated.

</details>

---

### 9. In NPS terminology, what does a **network policy** define?

* [ ] Firewall port configuration
* [ ] Rules that determine who can connect and under what conditions
* [ ] Network Address Translation (NAT) rules
* [ ] DNS zone parameters

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Rules that determine who can connect and under what conditions
💡 Network policies evaluate conditions, constraints, and settings to allow or deny access.

</details>

---

### 10. For centralized domain-based authentication, NPS commonly integrates with which service?

* [ ] Microsoft Excel
* [ ] Active Directory Domain Services
* [ ] Notepad++
* [ ] IIS Web Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active Directory Domain Services
💡 AD DS provides user credentials and group membership used in NPS policy evaluation.

</details>

---

### 11. In NPS configuration, a **RADIUS client** typically refers to which entity?

* [ ] An end-user workstation
* [ ] A DHCP server
* [ ] A Network Access Server (NAS)
* [ ] A web proxy server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A Network Access Server (NAS)
💡 Devices like VPN servers, wireless controllers, or switches act as RADIUS clients.

</details>

---

### 12. Which UDP port is used by RADIUS for authentication requests by default?

* [ ] 22
* [ ] 53
* [ ] 1812
* [ ] 80

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1812
💡 UDP 1812 is the IANA-assigned port for RADIUS authentication.

</details>

---

### 13. What is the default behavior if a connection request does **not match any connection request policy** in NPS?

* [ ] It is forwarded to DNS
* [ ] It is logged and denied
* [ ] It is automatically allowed
* [ ] It is redirected to DHCP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It is logged and denied
💡 NPS follows a deny-by-default model when no policy matches.

</details>

---

### 14. Which authentication methods are supported by NPS?

* [ ] Only PAP
* [ ] Only EAP
* [ ] PAP, CHAP, MS-CHAP, MS-CHAPv2, and EAP
* [ ] Only hardware token-based methods

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PAP, CHAP, MS-CHAP, MS-CHAPv2, and EAP
💡 NPS supports multiple authentication protocols depending on security requirements.

</details>

---

### 15. How can an administrator effectively monitor authentication and authorization events processed by NPS?

* [ ] Using WordPad
* [ ] Through Event Viewer
* [ ] Using Notepad
* [ ] Through Control Panel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Through Event Viewer
💡 NPS logs detailed operational and security events in Windows Event Viewer.

</details>

---

### 16. Before NPS can authenticate domain users, what must be registered in Active Directory?

* [ ] Local Users and Groups
* [ ] DNS host records
* [ ] NPS server
* [ ] Internet Explorer settings

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NPS server
💡 Registering NPS in AD allows it to read user account properties for authentication.

</details>

---

### 17. In an NPS deployment, what is the function of a **RADIUS proxy**?

* [ ] Encrypt local disk volumes
* [ ] Forward authentication requests to other RADIUS servers
* [ ] Apply Group Policy settings
* [ ] Assign IP addresses to clients

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forward authentication requests to other RADIUS servers
💡 RADIUS proxies are used in multi-forest or multi-site environments.

</details>

---

### 18. What is the primary purpose of a **health policy** in NPS?

* [ ] Email virus scanning
* [ ] VPN tunnel establishment
* [ ] Ensuring clients meet security compliance requirements
* [ ] Managing operating system updates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ensuring clients meet security compliance requirements
💡 Health policies are used with Network Access Protection (NAP).

</details>

---

### 19. What effect do **conditions** specified in a network policy have?

* [ ] They deny all access
* [ ] They determine which connections the policy applies to
* [ ] They update antivirus definitions
* [ ] They restart the NPS service

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They determine which connections the policy applies to
💡 Conditions filter requests based on user, device, time, and other attributes.

</details>

---

### 20. Which of the following is **NOT** typically used as a network policy condition?

* [ ] Day and time restrictions
* [ ] Client IP address
* [ ] Printer availability
* [ ] User group membership

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Printer availability
💡 Network policies focus on authentication and access parameters, not peripheral availability.

</details>

---

### 21. Which log file format is commonly used by NPS for detailed authentication and accounting records?

* [ ] system.log
* [ ] netlogon.dns
* [ ] IAS log
* [ ] firewall.evtx

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IAS log
💡 NPS evolved from Internet Authentication Service (IAS) and retains IAS-formatted logs.

</details>

---

### 22. What is the primary function of **NPS SQL logging**?

* [ ] Automatically delete old logs
* [ ] Store NPS logs in SQL Server for centralized reporting
* [ ] Compress Windows Event Logs
* [ ] Export configuration to Excel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Store NPS logs in SQL Server for centralized reporting
💡 SQL logging enables advanced auditing, billing, and compliance reporting.

</details>

---

### 23. In a multi-site enterprise, which component enables NPS to forward requests to another RADIUS server?

* [ ] DNS records
* [ ] Connection Request Policy
* [ ] Network Load Balancing (NLB)
* [ ] NTFS permissions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Connection Request Policy
💡 These policies determine whether requests are handled locally or forwarded.

</details>

---

### 24. How does NPS use **RADIUS attributes** within network policies?

* [ ] To define access time only
* [ ] To customize authorization and accounting responses
* [ ] To block internet usage
* [ ] To assign file system permissions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To customize authorization and accounting responses
💡 Attributes control parameters such as VLAN assignment, session timeout, and QoS.

</details>

---

### 25. Which RADIUS attribute is commonly used to assign a user to a specific VLAN?

* [ ] Class
* [ ] NAS-IP-Address
* [ ] Framed-IP-Address
* [ ] Tunnel-Private-Group-ID

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tunnel-Private-Group-ID
💡 This attribute specifies the VLAN ID for dynamic VLAN assignment.

</details>

---

### 26. What is a key advantage of deploying **multiple NPS servers**?

* [ ] Causes load imbalance
* [ ] Increases attack surface
* [ ] Provides redundancy and load balancing
* [ ] Disables network access control

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provides redundancy and load balancing
💡 Multiple NPS servers improve availability and scalability.

</details>

---

### 27. Which method is best suited for automating NPS configuration across multiple environments?

* [ ] Microsoft Paint
* [ ] Excel Macros
* [ ] PowerShell scripts
* [ ] Control Panel settings

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PowerShell scripts
💡 PowerShell allows scripted, repeatable, and version-controlled NPS deployments.

</details>

---

### 28. How can NPS differentiate between acting as a RADIUS server and a RADIUS proxy on the same system?

* [ ] Using Control Panel
* [ ] Installing separate server roles
* [ ] Configuring specific connection request policies
* [ ] Assigning different static IP addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configuring specific connection request policies
💡 Policy logic determines whether requests are processed locally or forwarded.

</details>

---

### 29. What role does NPS play in **Network Access Protection (NAP)**?

* [ ] Managing DHCP scopes
* [ ] Isolating compromised endpoints
* [ ] Enforcing health compliance before granting access
* [ ] Distributing digital certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enforcing health compliance before granting access
💡 NPS evaluates health policies to ensure compliance before allowing connectivity.

</details>

---

### 30. Which NPS feature enables tracking of user sessions for billing, auditing, or usage analysis?

* [ ] Network Discovery
* [ ] Traffic Monitor
* [ ] RADIUS Accounting
* [ ] Task Scheduler

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RADIUS Accounting
💡 RADIUS accounting records session start, stop, and usage data.

</details>

---

## **Session 17: Concept of Network Load Balancing (NLB)**

---

### 1. In a Windows Server environment, the acronym **NLB** refers to which clustering technology primarily designed for scalability and availability?

* [ ] Network Listening Base
* [ ] Net Level Backup
* [ ] Network Load Balancing
* [ ] Node Load Backup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Load Balancing
💡 NLB is a Windows Server feature used to distribute client traffic across multiple servers to ensure high availability and scalability.

</details>

---

### 2. An organization wants to distribute incoming HTTP requests across multiple identical web servers without shared storage. Which Windows Server role best satisfies this requirement?

* [ ] File Server
* [ ] DHCP Server
* [ ] Network Load Balancing (NLB)
* [ ] DNS Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Load Balancing (NLB)
💡 NLB operates at the network layer and distributes traffic without requiring shared disks or stateful clustering.

</details>

---

### 3. Which primary problem does Windows Server NLB aim to solve in enterprise deployments?

* [ ] Increasing disk throughput
* [ ] Encrypting inter-server traffic
* [ ] Distributing client network traffic
* [ ] Centralizing identity management

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Distributing client network traffic
💡 NLB improves availability and scalability by spreading incoming traffic across multiple hosts.

</details>

---

### 4. What is the **minimum number of hosts** required to form a functional NLB cluster?

* [ ] 4
* [ ] 2
* [ ] 1
* [ ] 3

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1
💡 NLB can technically run on a single node, though redundancy benefits are realized only with multiple nodes.

</details>

---

### 5. NLB is most appropriately deployed on which type of server workloads?

* [ ] Print servers
* [ ] Application and web servers
* [ ] Backup servers
* [ ] Domain controllers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Application and web servers
💡 NLB is ideal for stateless or loosely stateful services such as HTTP, HTTPS, and application front-ends.

</details>

---

### 6. Which architectural advantage is directly achieved by implementing NLB?

* [ ] Data-at-rest encryption
* [ ] Kerberos authentication
* [ ] High availability and horizontal scalability
* [ ] Network address translation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** High availability and horizontal scalability
💡 NLB allows additional hosts to be added dynamically to handle increased load and failures.

</details>

---

### 7. Which administrative interface is commonly used to configure and manage NLB in Windows Server?

* [ ] Disk Management
* [ ] Server Manager
* [ ] Hyper-V Manager
* [ ] Task Scheduler

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server Manager
💡 NLB is configured via Server Manager or PowerShell using the NLB feature.

</details>

---

### 8. NLB relies on which protocol stack to distribute client requests?

* [ ] FTP
* [ ] SNMP
* [ ] TCP/IP
* [ ] SMB

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TCP/IP
💡 NLB works at the IP and transport layers, distributing TCP/UDP traffic.

</details>

---

### 9. Which NLB mode allows all cluster hosts to receive traffic sent to the same virtual IP address?

* [ ] Unicast
* [ ] Multicast
* [ ] Broadcast
* [ ] Anycast

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multicast
💡 Multicast assigns a multicast MAC address, allowing hosts to receive traffic for the same IP.

</details>

---

### 10. Which NLB operation mode is most commonly associated with **switch flooding** issues?

* [ ] IGMP Multicast
* [ ] Unicast
* [ ] Anycast
* [ ] Multihoming

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Unicast
💡 Unicast replaces the MAC address, causing switches to flood traffic to all ports.

</details>

---

### 11. When a failed NLB host comes back online and rejoins the cluster automatically, which process enables this behavior?

* [ ] Convergence
* [ ] Load thresholding
* [ ] Failback
* [ ] Session replication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Convergence
💡 Convergence recalculates load distribution when cluster membership changes.

</details>

---

### 12. At which OSI layer does NLB primarily operate?

* [ ] Layer 2
* [ ] Layer 7
* [ ] Layer 4
* [ ] Layer 1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Layer 4
💡 NLB uses TCP/UDP port rules, placing it at the transport layer.

</details>

---

### 13. In NLB terminology, what is a **port rule**?

* [ ] A firewall ACL
* [ ] A DNS mapping
* [ ] A rule defining how traffic for specific ports is distributed
* [ ] A Group Policy object

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A rule defining how traffic for specific ports is distributed
💡 Port rules define filtering mode, affinity, and load percentage per port range.

</details>

---

### 14. How does an NLB cluster decide which host will service a particular client request?

* [ ] DNS forwarding
* [ ] Proxy chaining
* [ ] Hashing algorithm based on port rules
* [ ] Application-layer redirection

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hashing algorithm based on port rules
💡 NLB uses a deterministic hashing algorithm to map client requests to hosts.

</details>

---

### 15. What occurs when an active NLB node unexpectedly fails?

* [ ] Entire cluster stops
* [ ] Traffic is redistributed among remaining nodes
* [ ] Client sessions are terminated permanently
* [ ] Cluster IP is released

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Traffic is redistributed among remaining nodes
💡 NLB automatically converges to redistribute traffic.

</details>

---

### 16. Which of the following is **not** a valid NLB cluster operation mode?

* [ ] Unicast
* [ ] Multicast
* [ ] Broadcast
* [ ] IGMP Multicast

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Broadcast
💡 Broadcast mode is not supported in Windows NLB.

</details>

---

### 17. What uniquely identifies an NLB cluster on the network?

* [ ] Cluster MAC address
* [ ] Computer name
* [ ] Host priority value
* [ ] Subnet mask

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Cluster MAC address
💡 The cluster MAC represents the virtual identity of the NLB cluster.

</details>

---

### 18. Which NLB configuration ensures that a client consistently reaches the same host?

* [ ] Port filtering
* [ ] DNS TTL
* [ ] Affinity settings
* [ ] Load weight

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Affinity settings
💡 Single or Class C affinity maintains session persistence.

</details>

---

### 19. What is the **maximum number of nodes** supported in a Windows Server NLB cluster?

* [ ] 16
* [ ] 8
* [ ] 32
* [ ] 64

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 32
💡 Windows NLB supports up to 32 hosts per cluster.

</details>

---

### 20. Why is **IGMP Multicast** preferred over basic Multicast mode?

* [ ] Enhances encryption
* [ ] Prevents switch flooding
* [ ] Enables DNS replication
* [ ] Improves memory usage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevents switch flooding
💡 IGMP limits multicast traffic to interested ports only.

</details>

---

### 21. Which network configuration must remain consistent across all NLB hosts?

* [ ] Default gateway
* [ ] Host name
* [ ] Subnet mask and cluster IP
* [ ] MAC address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Subnet mask and cluster IP
💡 Inconsistent network settings break cluster communication.

</details>

---

### 22. What is the major limitation of **Unicast mode** in NLB?

* [ ] No failover support
* [ ] Hosts cannot communicate on the same subnet
* [ ] Requires static IPs
* [ ] Limited node count

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hosts cannot communicate on the same subnet
💡 Unicast replaces MAC addresses, breaking host-to-host communication.

</details>

---

### 23. How does NLB support session persistence for web applications?

* [ ] NAT translation
* [ ] Round-robin routing
* [ ] Affinity (Single or Class C)
* [ ] Port forwarding

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Affinity (Single or Class C)
💡 Affinity binds client requests to the same host.

</details>

---

### 24. Which event triggers NLB **convergence**?

* [ ] Firewall rule change
* [ ] Host joining or leaving the cluster
* [ ] Subnet modification
* [ ] IP address conflict

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Host joining or leaving the cluster
💡 Convergence recalculates load when membership changes.

</details>

---

### 25. How is load distribution calculated in NLB?

* [ ] Random allocation
* [ ] Least connections
* [ ] Host priority and port rule weights
* [ ] DNS round-robin

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Host priority and port rule weights
💡 NLB uses a weighted hashing algorithm.

</details>

---

### 26. What is the purpose of a **Dedicated IP address** in NLB?

* [ ] Shared client traffic
* [ ] Cluster virtual address
* [ ] Host-specific management communication
* [ ] Backup routing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Host-specific management communication
💡 Dedicated IP allows individual host administration.

</details>

---

### 27. Which application type is **least suitable** for NLB?

* [ ] Stateless web applications
* [ ] File sharing services
* [ ] Media streaming
* [ ] REST APIs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File sharing services
💡 File services require shared storage and state consistency, better suited for Failover Clustering.

</details>

---

### 28. Which PowerShell cmdlet is used to add a node to an NLB cluster?

* [ ] Add-NlbClusterNode
* [ ] Install-WindowsFeature
* [ ] Enable-NetAdapter
* [ ] Set-NetFirewallRule

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Add-NlbClusterNode
💡 This cmdlet explicitly manages NLB cluster membership.

</details>

---

### 29. In Unicast mode, what must be configured to allow inter-host communication?

* [ ] Disable MAC filtering
* [ ] Secondary NIC or hub
* [ ] DNS suffix
* [ ] IPv6 tunneling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Secondary NIC or hub
💡 A second interface restores host-to-host communication.

</details>

---

### 30. In large enterprise deployments, how is NLB health typically monitored?

* [ ] SNMP traps only
* [ ] Task Manager
* [ ] Packet capture tools
* [ ] Event Viewer and Performance Monitor

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Event Viewer and Performance Monitor
💡 These tools provide cluster state, convergence events, and performance metrics.

</details>

---

## **Session 17: Troubleshooting**

---

---

### 1. A Windows user reports frequent minor system issues such as audio failure and printer not responding. Which built-in Windows utility is specifically designed to automatically diagnose and resolve such common problems with minimal user intervention?

* [ ] To install and update hardware drivers
* [ ] To detect and fix common issues automatically
* [ ] To remove unused applications
* [ ] To manually configure advanced network parameters

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To detect and fix common issues automatically
💡 The Windows Troubleshooter is designed to automatically identify and resolve common OS-level issues such as sound, printer, and network problems without manual configuration.

</details>

---

### 2. On modern Windows 10 systems with UEFI and fast boot enabled, which method is most reliably used to access Safe Mode?

* [ ] Pressing F2 during POST
* [ ] Interrupting boot and accessing Advanced Startup options
* [ ] Pressing Esc repeatedly during startup
* [ ] Pressing Del to enter BIOS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Interrupting boot and accessing Advanced Startup options
💡 Due to fast boot and UEFI, traditional keys like F8 are disabled. Safe Mode is accessed via Advanced Startup (Shift + Restart or recovery options).

</details>

---

### 3. A network administrator uses the `ping` command while troubleshooting connectivity between two hosts. What is the primary function of this command?

* [ ] Measuring CPU response time
* [ ] Verifying disk I/O latency
* [ ] Testing network connectivity and latency
* [ ] Validating DNS zone transfers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Testing network connectivity and latency
💡 `ping` uses ICMP echo requests to verify reachability and measure round-trip time between hosts.

</details>

---

### 4. A system administrator wants to analyze system crashes and security-related events. From where can the Event Viewer be accessed most appropriately?

* [ ] Control Panel → System
* [ ] Settings → Applications
* [ ] Administrative Tools
* [ ] Task Manager → Startup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Administrative Tools
💡 Event Viewer is available under Windows Administrative Tools and provides detailed logs for system, security, and application events.

</details>

---

### 5. Which Windows utility provides real-time graphical visualization of CPU, memory, disk, and network performance counters?

* [ ] Disk Cleanup
* [ ] Performance Monitor
* [ ] Windows Defender
* [ ] Device Manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Performance Monitor
💡 Performance Monitor allows administrators to analyze system performance using counters, logs, and graphs.

</details>

---

### 6. A system administrator needs to immediately terminate an unresponsive application without triggering the security screen. Which keyboard shortcut directly opens Task Manager?

* [ ] Ctrl + Alt + Del
* [ ] Ctrl + Shift + Esc
* [ ] Alt + F4
* [ ] Windows + L

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ctrl + Shift + Esc
💡 This shortcut opens Task Manager directly, bypassing intermediate screens.

</details>

---

### 7. An application stops responding but the operating system remains stable. What is the most appropriate first troubleshooting action?

* [ ] Restart the entire system
* [ ] Open File Explorer
* [ ] End the application process using Task Manager
* [ ] Format the system drive

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** End the application process using Task Manager
💡 Terminating the hung process isolates the issue without disrupting the entire system.

</details>

---

### 8. A Windows administrator suspects corruption of protected system files. Which command-line utility should be executed first to verify and repair them?

* [ ] chkdsk
* [ ] sfc /scannow
* [ ] netstat
* [ ] ipconfig

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** sfc /scannow
💡 System File Checker scans and restores corrupted protected system files using cached copies.

</details>

---

### 9. Which Windows management console is primarily used to troubleshoot malfunctioning hardware components and driver-related issues?

* [ ] Network and Sharing Center
* [ ] Hardware drivers and devices
* [ ] BIOS setup utility
* [ ] Malware protection dashboard

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hardware drivers and devices
💡 Device Manager provides status, driver versions, and error codes for installed hardware.

</details>

---

### 10. Which of the following is NOT a default log category in Windows Event Viewer?

* [ ] Application
* [ ] Security
* [ ] Network
* [ ] System

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network
💡 Event Viewer primarily contains Application, Security, System, and Setup logs.

</details>

---

### 11. A system becomes unstable after a driver update. Which Windows feature allows reverting system files and registry settings to an earlier stable state?

* [ ] Disk Management
* [ ] System Restore
* [ ] Startup Settings
* [ ] Task Scheduler

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** System Restore
💡 System Restore uses restore points to revert system configuration without affecting personal files.

</details>

---

### 12. A faulty driver is preventing normal startup. Which boot option minimizes loaded drivers to aid troubleshooting?

* [ ] Safe Mode
* [ ] Normal Mode
* [ ] Sleep Mode
* [ ] Hibernate Mode

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Safe Mode
💡 Safe Mode loads only essential drivers and services, making it ideal for driver-related issues.

</details>

---

### 13. Which command provides comprehensive details such as MAC address, DHCP status, and DNS servers?

* [ ] nslookup
* [ ] ipconfig /all
* [ ] net use
* [ ] ping -t

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ipconfig /all
💡 This command displays full TCP/IP configuration details.

</details>

---

### 14. A Blue Screen of Death (BSOD) in Windows most commonly indicates which underlying issue?

* [ ] Incorrect display resolution
* [ ] Excessive background applications
* [ ] Hardware or driver failure
* [ ] Browser misconfiguration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hardware or driver failure
💡 BSODs typically occur due to kernel-level faults caused by hardware or drivers.

</details>

---

### 15. Which Windows utility is used to create, delete, and resize disk partitions?

* [ ] msconfig
* [ ] Task Manager
* [ ] Disk Management
* [ ] services.msc

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Disk Management
💡 Disk Management provides graphical disk and volume administration.

</details>

---

### 16. What is the primary administrative purpose of the `msconfig` utility?

* [ ] Software installation
* [ ] Printer configuration
* [ ] Startup and boot configuration
* [ ] Network traffic monitoring

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Startup and boot configuration
💡 msconfig allows selective startup, boot logging, and service control.

</details>

---

### 17. In Task Manager, sustained high disk usage most commonly indicates:

* [ ] Expired antivirus definitions
* [ ] Insufficient RAM only
* [ ] Heavy read/write operations on storage
* [ ] Multiple USB peripherals connected

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Heavy read/write operations on storage
💡 High disk usage reflects I/O bottlenecks, paging, or background services.

</details>

---

### 18. Which command-line tool is best suited for diagnosing DNS resolution problems?

* [ ] ping
* [ ] nslookup
* [ ] netstat
* [ ] tracert

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** nslookup
💡 nslookup queries DNS servers directly to diagnose name resolution issues.

</details>

---

### 19. What is the primary function of the DISM (Deployment Image Servicing and Management) tool?

* [ ] Remove temporary files
* [ ] Mount and repair Windows images
* [ ] Display memory usage
* [ ] Power off the system

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mount and repair Windows images
💡 DISM repairs Windows component stores and offline/online images.

</details>

---

### 20. A single user cannot connect to Wi-Fi, while others on the same network can. What is the most logical first troubleshooting step?

* [ ] Restart the router
* [ ] Restart the affected user’s system
* [ ] Reinstall the operating system
* [ ] Disable the firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Restart the affected user’s system
💡 The issue is isolated to one host, so local troubleshooting is appropriate.

</details>

---

### 21. Which boot option allows administrators to observe which drivers and services are loaded during startup?

* [ ] Safe Mode
* [ ] Debugging Mode
* [ ] Last Known Good Configuration
* [ ] Verbose Boot

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Debugging Mode
💡 Debugging mode provides low-level startup diagnostics useful for driver analysis.

</details>

---


### 22. What is the technical effect of executing `netsh winsock reset` on a Windows system?

* [ ] Resets browser configuration
* [ ] Clears temporary system files
* [ ] Resets network sockets to default state
* [ ] Removes and reinstalls NIC drivers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Resets network sockets to default state
💡 It repairs corrupted Winsock entries that can disrupt network connectivity.

</details>

---

### 23. If Windows fails to boot and Safe Mode is inaccessible, which recovery option is most appropriate next?

* [ ] Wait indefinitely for automatic repair
* [ ] Use System Restore from Windows Recovery Environment
* [ ] Delete the System32 directory
* [ ] Disable antivirus from BIOS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use System Restore from Windows Recovery Environment
💡 WinRE allows restoring a previously functional system state safely.

</details>

---

### 24. Windows error code `0x80070057` generally indicates:

* [ ] Expired antivirus subscription
* [ ] Network unavailability
* [ ] Invalid parameter or disk-related issue
* [ ] Printer spooler failure

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Invalid parameter or disk-related issue
💡 Commonly associated with incorrect arguments or file system corruption.

</details>

---

### 25. What is the primary purpose of the Windows Reliability Monitor?

* [ ] Monitoring RAM consumption
* [ ] Displaying real-time network throughput
* [ ] Tracking system stability over time
* [ ] Editing registry keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tracking system stability over time
💡 Reliability Monitor provides a timeline of crashes, updates, and failures.

</details>

---

### 26. Which utility is most effective for detecting logical file system errors and bad sectors on a hard drive?

* [ ] Event Viewer
* [ ] Task Manager
* [ ] CHKDSK
* [ ] services.msc

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CHKDSK
💡 CHKDSK scans and repairs disk file system errors and bad sectors.

</details>

---

### 27. When executing the `tracert` command, what information is being analyzed?

* [ ] Disk access paths
* [ ] DNS resolution sequence
* [ ] Network path packets take to the destination
* [ ] Firewall filtering rules

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network path packets take to the destination
💡 tracert identifies intermediate hops and latency along a network route.

</details>

---

### 28. Which Windows utility verifies the authenticity and digital signatures of installed drivers?

* [ ] Device Manager
* [ ] File Explorer
* [ ] sigverif.exe
* [ ] gpedit.msc

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** sigverif.exe
💡 Signature Verification Tool checks for unsigned or tampered drivers.

</details>

---

### 29. Which PowerShell command is specifically used to detect and repair corruption in the Windows image?

* [ ] Get-Process
* [ ] Repair-WindowsImage
* [ ] New-NetIPAddress
* [ ] Get-DnsClientServerAddress

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Repair-WindowsImage
💡 This cmdlet works with DISM to repair component store corruption.

</details>

---

### 30. In a domain environment, which tool provides the most comprehensive diagnosis of Group Policy application issues?

* [ ] Group Policy Editor
* [ ] gpresult /h report.html
* [ ] Event Viewer
* [ ] Active Directory Users and Computers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** gpresult /h report.html
💡 gpresult generates a detailed HTML report showing applied and failed GPOs.

</details>

---

