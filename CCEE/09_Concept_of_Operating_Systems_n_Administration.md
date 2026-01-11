> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 09

## **Session 10: Concept of IIS Web Server**

---

### 1. In the context of Windows Server, what does IIS stand for?

* [ ] Internet Intranet Server
* [ ] Internet Information Services
* [ ] Internal Information Software
* [ ] Integrated Internet System

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Internet Information Services
💡 IIS is Microsoft’s web server platform for hosting websites and web applications on Windows servers. It provides HTTP, HTTPS, FTP, and other web-related services.

</details>

---

### 2. A company wants to host multiple web applications on a Windows Server. Which of the following best describes IIS’s primary purpose?

* [ ] Games
* [ ] Web applications and websites
* [ ] Mobile apps
* [ ] File sharing networks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Web applications and websites
💡 IIS is designed to host web applications (ASP.NET, PHP, etc.) and websites. It is not meant for hosting mobile apps directly or general file-sharing.

</details>

---

### 3. Which version of Windows Server first included IIS?

* [ ] Windows Server 2000
* [ ] Windows NT 3.51
* [ ] Windows XP
* [ ] Windows 7

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Windows NT 3.51
💡 IIS was first introduced as an optional component in Windows NT 3.51, enabling HTTP and FTP services. Later versions of Windows Server included it by default.

</details>

---

### 4. A developer configures a website in IIS. By default, which port will IIS listen on for HTTP traffic?

* [ ] 80
* [ ] 21
* [ ] 443
* [ ] 25

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 80
💡 Port 80 is the default for HTTP traffic. Port 443 is used for HTTPS, 21 for FTP, and 25 for SMTP.

</details>

---

### 5. Which Microsoft tool provides a GUI specifically for managing IIS services and websites?

* [ ] PowerShell
* [ ] IIS Manager
* [ ] Control Panel
* [ ] Event Viewer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IIS Manager
💡 IIS Manager is a graphical interface designed to configure sites, application pools, security, and logging. PowerShell can automate IIS but is command-line based.

</details>

---

### 6. An organization wants to host a mix of static HTML, ASP.NET, and PHP websites. Which option correctly describes IIS’s capabilities?

* [ ] Only static HTML
* [ ] Only ASP.NET
* [ ] HTML, ASP.NET, PHP and others
* [ ] Only PHP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HTML, ASP.NET, PHP and others
💡 IIS supports multiple web technologies, including static HTML, dynamic ASP.NET, PHP, and CGI-based applications, making it versatile for enterprise web hosting.

</details>

---

### 7. Which Windows service must be running for IIS to operate correctly?

* [ ] Windows Update
* [ ] IIS Admin Service
* [ ] Print Spooler
* [ ] Remote Desktop Services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IIS Admin Service
💡 The IIS Admin Service manages web services. If it is stopped, websites and application pools cannot start.

</details>

---

### 8. Which protocol is used by IIS for secure communication over the web?

* [ ] FTP
* [ ] SFTP
* [ ] HTTPS
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HTTPS
💡 HTTPS uses SSL/TLS to encrypt web traffic between clients and the IIS server. FTP/SFTP are for file transfers, and SNMP is for network monitoring.

</details>

---

### 9. In IIS, what component is responsible for isolating web applications to improve security and stability?

* [ ] Application Pool
* [ ] Virtual Directory
* [ ] Windows Firewall
* [ ] Site Binding

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Application Pool
💡 Application pools isolate websites or applications in separate worker processes, preventing one app’s failure from affecting others.

</details>

---

### 10. A web administrator wants to map a folder on a different disk as part of a website. Which IIS feature supports this?

* [ ] A directory on another server
* [ ] A directory that redirects to the recycle bin
* [ ] A directory mapped to a different location on disk
* [ ] A folder without physical existence

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A directory mapped to a different location on disk
💡 Virtual directories allow administrators to link folders outside the default web root into a website’s URL structure.

</details>

---


### 11. A system administrator needs to install IIS on a new Windows Server. Which method is the standard and recommended approach?

* [ ] Through Disk Management
* [ ] With Server Manager > Add Roles and Features
* [ ] By downloading from Microsoft Store
* [ ] Using Windows Update

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** With Server Manager > Add Roles and Features
💡 IIS is installed as a server role via Server Manager. This method ensures all dependencies and features are correctly configured.

</details>

---

### 12. Which port does IIS use by default for HTTPS traffic?

* [ ] 21
* [ ] 443
* [ ] 80
* [ ] 53

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 443
💡 HTTPS encrypts web traffic using SSL/TLS. By default, IIS listens for HTTPS requests on port 443.

</details>

---

### 13. How does an IIS Application Pool enhance web application security and performance?

* [ ] Deletes unused applications
* [ ] Isolates web applications for security and performance
* [ ] Stores FTP files
* [ ] Displays real-time visitor statistics

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Isolates web applications for security and performance
💡 Each application pool runs in a separate worker process (w3wp.exe). This isolation prevents one application from affecting others and allows tailored process settings.

</details>

---

### 14. By default, which types of files can IIS serve without additional configuration?

* [ ] .exe
* [ ] .dll
* [ ] .html, .css, .js
* [ ] .msi

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .html, .css, .js
💡 IIS natively serves common web file types like HTML, CSS, and JavaScript. Executable files or DLLs require special handling for security reasons.

</details>

---

### 15. Which server-side scripting technology is natively supported by IIS for dynamic web content?

* [ ] Python
* [ ] JavaScript only
* [ ] ASP.NET
* [ ] C++

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ASP.NET
💡 IIS tightly integrates with ASP.NET to process dynamic web pages. While Python or PHP can work via extensions, ASP.NET is native.

</details>

---

### 16. An administrator wants to automate repetitive IIS tasks via command-line. Which tool is suitable for this?

* [ ] Notepad
* [ ] PowerShell
* [ ] Paint
* [ ] Excel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PowerShell
💡 PowerShell supports cmdlets specifically for IIS management, including creating sites, managing application pools, and configuring settings programmatically.

</details>

---

### 17. In an ASP.NET web application hosted on IIS, what is the purpose of the Web.config file?

* [ ] A configuration file for database
* [ ] A text file to store images
* [ ] A settings file for ASP.NET apps
* [ ] An email configuration file

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A settings file for ASP.NET apps
💡 Web.config contains configuration settings such as authentication, authorization, session state, and connection strings for ASP.NET applications.

</details>

---

### 18. By default, where does IIS store log files on a Windows Server?

* [ ] C:\Program Files\IIS
* [ ] C:\inetpub\logs\LogFiles
* [ ] D:\SystemLogs
* [ ] C:\Users\Public\Documents

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** C:\inetpub\logs\LogFiles
💡 IIS writes request logs here by default. Logs help administrators troubleshoot errors, monitor traffic, and analyze website usage.

</details>

---

### 19. In IIS, what does “binding” refer to when configuring a website?

* [ ] File encryption
* [ ] Memory allocation
* [ ] Mapping IP address, port, and protocol
* [ ] Folder permissions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mapping IP address, port, and protocol
💡 Binding associates a website with an IP, port, and optionally a host header, allowing multiple sites to run on the same server.

</details>

---

### 20. Which IIS authentication method integrates with Active Directory to provide single sign-on for users?

* [ ] Basic
* [ ] Anonymous
* [ ] Windows Authentication
* [ ] Digest

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Windows Authentication
💡 Windows Authentication uses Kerberos or NTLM protocols to authenticate users with their Active Directory credentials, enabling SSO for intranet applications.

</details>

---

### 21. What IIS feature allows administrators to control user access to specific web content?

* [ ] Authorization Rules
* [ ] Server Manager
* [ ] Event Viewer
* [ ] App Pool Recycling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authorization Rules
💡 Authorization Rules define which users or groups can access specific files or folders in IIS, enhancing security for web applications.

</details>

---

### 22. An enterprise wants users to manage files on a website remotely via HTTP. Which IIS feature should be enabled?

* [ ] Monitor CPU usage
* [ ] WebDAV
* [ ] Generate SSL certificates
* [ ] Create backups

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** WebDAV
💡 WebDAV (Web Distributed Authoring and Versioning) allows authorized users to remotely create, read, update, and delete files over HTTP/HTTPS. It is not related to monitoring CPU, SSL generation, or backups.

</details>

---

### 23. A developer sends a request to an IIS-hosted API, which processes successfully but intentionally returns no content. Which HTTP status code does IIS return?

* [ ] 200
* [ ] 204
* [ ] 404
* [ ] 500

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 204
💡 HTTP 204 indicates that the request was successful but there is no content to return. 200 implies success with content, 404 is "Not Found," and 500 indicates a server error.

</details>

---

### 24. A system administrator needs to host multiple websites on a single IIS server without conflicts. How should this be configured?

* [ ] Using only one application pool
* [ ] Using DNS round-robin
* [ ] By using unique bindings (host headers, IPs, or ports)
* [ ] By installing multiple IIS instances

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** By using unique bindings (host headers, IPs, or ports)
💡 IIS allows multiple websites on the same server by assigning each site a unique combination of IP, port, or host header. This avoids conflicts while using the same application pool or instance.

</details>

---

### 25. How does configuring Process Model settings in an IIS Application Pool benefit web applications?

* [ ] Define recycling frequency only
* [ ] Control how worker processes are started and managed
* [ ] Log user credentials
* [ ] Connect to SQL Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Control how worker processes are started and managed
💡 Process Model settings define identity, startup behavior, recycling, idle timeout, and maximum worker processes, improving stability and performance.

</details>

---

### 26. Which IIS feature ensures secure transmission of web traffic between clients and the server?

* [ ] IP Filtering
* [ ] SSL Binding
* [ ] Static Content Compression
* [ ] HTTP Redirect

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSL Binding
💡 SSL Binding links an SSL certificate to a website or application in IIS, enabling HTTPS and encrypting all client-server communication.

</details>

---

### 27. How does the IIS Dynamic IP Restrictions feature help protect websites?

* [ ] IP spoofing
* [ ] Port scanning
* [ ] Denial of Service (DoS) attacks
* [ ] Email spam

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Denial of Service (DoS) attacks
💡 Dynamic IP Restrictions monitor client request rates and block excessive requests from a single IP, mitigating DoS or brute-force attacks.

</details>

---

### 28. An administrator sets an application pool to "AlwaysRunning." What effect does this configuration have?

* [ ] Automatically disables the site
* [ ] Keeps the worker process in memory
* [ ] Increases website bandwidth
* [ ] Forces HTTPS on all sites

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Keeps the worker process in memory
💡 "AlwaysRunning" ensures the application pool worker process remains active, reducing cold-start delays for applications and improving response time.

</details>

---

### 29. A company wants all old URLs to redirect to new ones while keeping query parameters intact. Which IIS feature should be used?

* [ ] Blocks traffic
* [ ] Logs URLs
* [ ] URL Rewrite module
* [ ] Encrypts content

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** URL Rewrite module
💡 The URL Rewrite module allows administrators to define rules for redirecting or rewriting URLs. This supports SEO, legacy links, and custom routing.

</details>

---

### 30. An administrator needs to export an IIS site configuration to migrate it to another server. Which command-line tool is appropriate?

* [ ] iisdiag
* [ ] iisreset
* [ ] appcmd
* [ ] iscsicli

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** appcmd
💡 `appcmd` is a command-line utility to manage IIS configurations, including exporting and importing site settings. `iisreset` restarts IIS, and `iisdiag` is for diagnostics.

</details>

---

## **Session 11: Concept of Core and Distributed Network Solutions**

---


### 1. What is the primary function of a core network in an enterprise environment?

* [ ] Connecting end-user devices in a home network
* [ ] Providing internet access to mobile users directly
* [ ] Interconnecting multiple subnetworks and managing high-speed traffic
* [ ] Storing backup files for disaster recovery

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Interconnecting multiple subnetworks and managing high-speed traffic
💡 The core network forms the backbone of enterprise or service provider networks, ensuring fast, reliable connectivity between distribution layers or subnetworks. It is not concerned with direct user device connections or storage.

</details>

---

### 2. Which scenario best illustrates a distributed network architecture?

* [ ] A single central server managing all operations
* [ ] Multiple interconnected servers across geographic locations collaborating
* [ ] A single private server serving a local office
* [ ] Isolated LANs in independent branches

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multiple interconnected servers across geographic locations collaborating
💡 Distributed networks distribute processing and resources across multiple nodes to increase reliability, scalability, and fault tolerance.

</details>

---

### 3. Which device is essential for directing high-speed traffic in the core of a network?

* [ ] Printer
* [ ] Basic switch
* [ ] Router
* [ ] Core switch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Core switch
💡 Core switches operate at the backbone layer, providing high-speed packet forwarding between distribution switches. Routers are used for inter-networking but core switches are central in high-speed LAN/WAN environments.

</details>

---

### 4. What is a primary advantage of implementing a distributed network over a centralized network?

* [ ] Centralized control
* [ ] Low scalability
* [ ] Fault tolerance and redundancy
* [ ] High maintenance cost

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fault tolerance and redundancy
💡 Distributed networks mitigate single points of failure and allow continued operation even if some nodes fail.

</details>

---

### 5. Which network topology inherently supports distributed networks by providing multiple paths between nodes?

* [ ] Star
* [ ] Ring
* [ ] Mesh
* [ ] Bus

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mesh
💡 Mesh topology provides multiple redundant paths between nodes, increasing reliability and fault tolerance in distributed systems.

</details>

---

### 6. In networking, what does latency primarily indicate?

* [ ] Speed of user input at the keyboard
* [ ] Size of a data packet
* [ ] Delay in data transmission between nodes
* [ ] Device operating temperature

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Delay in data transmission between nodes
💡 Latency measures the time a packet takes to travel from source to destination. Minimizing latency is crucial in core and distributed networks for performance.

</details>

---

### 7. Which OSI layer is chiefly responsible for routing decisions in a core network?

* [ ] Data Link Layer
* [ ] Network Layer
* [ ] Transport Layer
* [ ] Application Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Layer
💡 The Network Layer handles logical addressing and path selection, making routing decisions for packets in large-scale core networks.

</details>

---

### 8. In a large-scale ISP network, which routing protocol is preferred for exchanging routes between autonomous systems?

* [ ] RIP
* [ ] OSPF
* [ ] BGP
* [ ] EIGRP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** BGP
💡 Border Gateway Protocol (BGP) is used for routing between autonomous systems in large-scale networks. OSPF is for intra-domain routing, RIP and EIGRP are unsuitable for very large, distributed networks.

</details>

---

### 9. A network engineer needs to aggregate multiple access-layer switches in a campus network. Which device is most appropriate for this distribution function?

* [ ] Core switch
* [ ] Access point
* [ ] Firewall
* [ ] Distribution/aggregation switch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Distribution/aggregation switch
💡 Distribution switches aggregate traffic from access switches and connect to core switches, acting as an intermediate layer between access and core layers.

</details>

---

### 10. Which is a defining characteristic of core layer devices in hierarchical network design?

* [ ] Low-speed communication
* [ ] Direct connection to end users
* [ ] High-speed packet switching with minimal processing
* [ ] Hosting applications and databases

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** High-speed packet switching with minimal processing
💡 Core devices focus on fast and reliable forwarding, not on direct user access or hosting services.

</details>

---

### 11. In a distributed network, where are DNS and DHCP services typically deployed for efficiency and scalability?

* [ ] Core layer
* [ ] Access layer
* [ ] Application layer
* [ ] Transport layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Core layer
💡 Core-layer placement ensures that critical services like DNS and DHCP are highly available and can serve all parts of the network efficiently.

</details>

---

### 12. Load balancing in a distributed server environment primarily ensures:

* [ ] Secure file storage
* [ ] Even distribution of client requests across servers
* [ ] Encryption of data in transit
* [ ] Blocking unauthorized users

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Even distribution of client requests across servers
💡 Load balancers optimize resource usage, improve performance, and prevent single-server overload in distributed systems.

</details>

---

### 13. For internal routing in a private distributed network, which IP addressing scheme is most suitable?

* [ ] Public IP addresses
* [ ] Static IP addresses only
* [ ] Loopback addresses
* [ ] Private IP addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Private IP addresses
💡 Private IP addresses are used internally to route traffic safely without exposing internal networks to the public internet.

</details>

---

### 14. In distributed systems, implementing redundancy primarily aims to:

* [ ] Reduce network speed
* [ ] Decrease reliability
* [ ] Increase fault tolerance and availability
* [ ] Save operational cost

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Increase fault tolerance and availability
💡 Redundancy ensures that if one component fails, another can take over, maintaining continuous service.

</details>

---

### 15. A “data center fabric” is best described as:

* [ ] A cooling mechanism for servers
* [ ] Hierarchical power supply design
* [ ] Network architecture optimizing east-west traffic between servers
* [ ] Structured cable management

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network architecture optimizing east-west traffic between servers
💡 Data center fabric designs reduce bottlenecks and improve server-to-server communication within a data center.

</details>

---

### 16. Why is data replication important in distributed environments?

* [ ] To prevent user access
* [ ] To increase latency intentionally
* [ ] To improve data availability and reliability
* [ ] To encrypt network packets

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To improve data availability and reliability
💡 Replication ensures that multiple copies of data exist across nodes, so failure at one site does not cause data loss.

</details>

---

### 17. Which protocol allows automatic IP address assignment in a distributed network?

* [ ] TCP
* [ ] ARP
* [ ] DHCP
* [ ] ICMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DHCP
💡 Dynamic Host Configuration Protocol (DHCP) assigns IP addresses dynamically to devices, simplifying management in distributed networks.

</details>

---

### 18. In data centers, “east-west traffic” refers to:

* [ ] Data flow between clients and the internet
* [ ] Traffic between geographically separate sites
* [ ] Server-to-server communication within the same data center
* [ ] Core-to-access layer communication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server-to-server communication within the same data center
💡 East-west traffic is internal, while north-south traffic flows between clients and core/internet.

</details>

---

### 19. Which protocol is commonly used to monitor and manage distributed network devices?

* [ ] VPN
* [ ] SNMP
* [ ] SMTP
* [ ] DNS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SNMP
💡 Simple Network Management Protocol (SNMP) allows centralized monitoring, fault detection, and performance management of network devices.

</details>

---

### 20. Spanning Tree Protocol (STP) is deployed in networks primarily to:

* [ ] Increase routing speed
* [ ] Encrypt network traffic
* [ ] Prevent Layer 2 loops
* [ ] Provide web access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevent Layer 2 loops
💡 STP disables redundant paths dynamically to avoid broadcast storms while maintaining network redundancy.

</details>

---

### 21. What is the key role of a distribution switch in a hierarchical network?

* [ ] Forwarding traffic at core speeds
* [ ] Authenticating end users
* [ ] Aggregating access-layer connections and connecting to the core
* [ ] Connecting directly to ISPs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Aggregating access-layer connections and connecting to the core
💡 Distribution switches consolidate traffic from access switches and relay it to the core layer efficiently.

</details>

---

### 22. A multinational company replicates its databases across continents. What is the main challenge it faces in keeping the data consistent?

* [ ] High storage costs
* [ ] Geographic diversity causing latency and synchronization issues
* [ ] Encryption protocol incompatibility
* [ ] Network naming conflicts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Geographic diversity causing latency and synchronization issues
💡 Distributed systems across multiple locations must handle propagation delays and conflicts, which can lead to temporary inconsistencies or “split-brain” scenarios.

</details>

---

### 23. Which protocol is most commonly used for interconnecting core networks between different ISPs on the Internet?

* [ ] RIP
* [ ] OSPF
* [ ] BGP
* [ ] IGMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** BGP
💡 Border Gateway Protocol (BGP) is designed for exchanging routing information between autonomous systems (inter-ISP), unlike RIP or OSPF which are intra-domain protocols.

</details>

---

### 24. In a distributed environment, Anycast addressing is primarily used to:

* [ ] Achieve one-to-one communication
* [ ] Make all servers respond simultaneously
* [ ] Direct client requests to the nearest available server
* [ ] Broadcast to all nodes in the network

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Direct client requests to the nearest available server
💡 Anycast allows multiple servers to share the same IP; routing directs traffic to the closest instance, reducing latency and improving resilience.

</details>

---

### 25. Which technology increases resilience and optimizes multiple WAN paths in distributed networks?

* [ ] VLAN
* [ ] SD-WAN
* [ ] MPLS
* [ ] NAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SD-WAN
💡 Software-Defined WAN dynamically chooses the best path for traffic across multiple links, enhancing redundancy, performance, and failover in distributed networks.

</details>

---

### 26. According to the CAP theorem in distributed systems, a network designer must consider trade-offs between:

* [ ] Cost, Access, Power
* [ ] Consistency, Availability, Partition Tolerance
* [ ] Control, Application, Portability
* [ ] Cache, API, Processing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Consistency, Availability, Partition Tolerance
💡 CAP theorem states that a distributed system can guarantee at most two of these properties simultaneously; designers must make trade-offs based on application needs.

</details>

---

### 27. In network traffic terminology, “north-south traffic” refers to:

* [ ] Server-to-server communication within a data center
* [ ] Data flow between clients and the core network or the Internet
* [ ] Traffic among cloud storage units
* [ ] Internal access-layer communication only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data flow between clients and the core network or the Internet
💡 North-south traffic moves in and out of the data center, while east-west traffic occurs internally between servers.

</details>

---

### 28. Which system design provides geographic redundancy for web applications to ensure low latency and high availability?

* [ ] DNS Round Robin
* [ ] Firewall
* [ ] VLAN
* [ ] Proxy server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS Round Robin
💡 Distributed DNS can direct users to the nearest server geographically, providing redundancy and reducing latency in multi-site deployments.

</details>

---

### 29. What is the primary benefit of implementing a distributed DNS architecture?

* [ ] Easier caching of domain records
* [ ] Faster database queries
* [ ] Reduced latency and improved fault tolerance
* [ ] Manual updates only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduced latency and improved fault tolerance
💡 Distributed DNS ensures requests are resolved by the closest or available server, minimizing latency and preventing service disruption in case of failures.

</details>

---

### 30. Which security risk is particularly critical in distributed networks compared to centralized systems?

* [ ] Malware infections
* [ ] Centralized authentication bypass
* [ ] Data inconsistency and split-brain scenarios
* [ ] Blue screen of death

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data inconsistency and split-brain scenarios
💡 In distributed systems, simultaneous updates or network partitions can lead to inconsistent data states, a risk largely absent in centralized architectures.

</details>

---
