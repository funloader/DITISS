> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 18

## **Session 18 : Linux OS**
---

### 1. In an enterprise Linux environment, what does **NTP** primarily stand for?

* [ ] Network Test Protocol
* [ ] Network Time Protocol
* [ ] New Transfer Protocol
* [ ] Node Transmission Path

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Time Protocol
💡 NTP is used to synchronize system clocks over packet-switched networks, which is critical for security logging, forensics, and distributed systems.

</details>

---

### 2. Why is accurate system time considered critical from a **security and forensic** perspective?

* [ ] It improves graphical display performance
* [ ] It ensures correct sequencing and correlation of log timestamps
* [ ] It reduces network latency
* [ ] It optimizes CPU scheduling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It ensures correct sequencing and correlation of log timestamps
💡 Accurate timestamps are essential for incident reconstruction, log correlation, and legal admissibility of digital evidence.

</details>

---

### 3. What is the **primary operational role** of BIND in a networked environment?

* [ ] File compression service
* [ ] DNS name resolution service
* [ ] Firewall policy enforcement
* [ ] Dynamic routing table generation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS name resolution service
💡 BIND (Berkeley Internet Name Domain) is the most widely used DNS server software, responsible for resolving domain names to IP addresses.

</details>

---

### 4. Which Linux log file typically records **authentication and authorization events**?

* [ ] /var/log/syslog
* [ ] /var/log/auth.log
* [ ] /etc/passwd
* [ ] /home/log.txt

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /var/log/auth.log
💡 This file logs SSH logins, sudo usage, and authentication failures, making it crucial for detecting unauthorized access.

</details>

---

### 5. Which network port does DNS primarily use for **standard query resolution**?

* [ ] 53
* [ ] 80
* [ ] 443
* [ ] 25

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 53
💡 DNS uses port 53 over UDP for most queries and TCP for zone transfers and large responses.

</details>

---

### 6. In DNS operations, what does a **DNS cache** store?

* [ ] Temporary firewall rules
* [ ] Recently resolved domain-to-IP mappings
* [ ] Browser configuration data
* [ ] Encrypted DNS packets

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Recently resolved domain-to-IP mappings
💡 DNS caching improves performance and reduces load but can be abused in cache poisoning attacks.

</details>

---

### 7. What is the primary function of **syslog** in Linux systems?

* [ ] User account management
* [ ] Memory allocation
* [ ] Centralized collection and storage of log messages
* [ ] Graphical interface rendering

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centralized collection and storage of log messages
💡 Syslog provides standardized logging across system components, essential for monitoring and incident response.

</details>

---

### 8. Which transport protocol is primarily used by NTP for time synchronization?

* [ ] UDP
* [ ] TCP
* [ ] HTTP
* [ ] FTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** UDP
💡 NTP uses UDP port 123 to minimize overhead and latency in time synchronization.

</details>

---

### 9. In NTP architecture, what does the **stratum value** represent?

* [ ] Number of connected clients
* [ ] Distance from the reference clock and relative accuracy
* [ ] Log file hierarchy
* [ ] Network bandwidth usage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Distance from the reference clock and relative accuracy
💡 Lower stratum numbers indicate closer proximity to authoritative time sources, such as atomic clocks.

</details>

---

### 10. Which file traditionally contains the **primary syslog configuration** on classic Linux systems?

* [ ] /etc/sysconfig/syslog.conf
* [ ] /etc/syslog.d
* [ ] /etc/syslog.conf
* [ ] /syslog/sys.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/syslog.conf
💡 While modern systems use rsyslog with /etc/rsyslog.conf, /etc/syslog.conf is the traditional configuration file.

</details>

---

### 11. In DNS administration, what is a **zone file**?

* [ ] A compressed log archive
* [ ] A DNS firewall rule list
* [ ] A file containing resource records for a domain
* [ ] A volatile memory dump

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A file containing resource records for a domain
💡 Zone files define mappings like A, AAAA, MX, and NS records for DNS resolution.

</details>

---

### 12. Which Linux command is most commonly used for **detailed DNS troubleshooting**?

* [ ] ls
* [ ] dig
* [ ] ps
* [ ] whoami

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dig
💡 `dig` provides verbose DNS query output, useful for diagnosing resolution and DNSSEC issues.

</details>

---

### 13. What is the default network port used by syslog for remote logging?

* [ ] 21
* [ ] 25
* [ ] 514
* [ ] 110

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 514
💡 Syslog traditionally uses UDP 514, though secure implementations may use TCP or TLS.

</details>

---

### 14. How does **DNSSEC** primarily enhance DNS security?

* [ ] By encrypting DNS queries
* [ ] By authenticating the origin and integrity of DNS data
* [ ] By replacing IP addressing
* [ ] By improving cache speed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** By authenticating the origin and integrity of DNS data
💡 DNSSEC uses cryptographic signatures to prevent DNS spoofing and cache poisoning.

</details>

---

### 15. Which BIND directive explicitly controls **zone transfer permissions**?

* [ ] allow-transfer
* [ ] zone-send
* [ ] named-transfer
* [ ] send-zone

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** allow-transfer
💡 Restricting zone transfers prevents attackers from harvesting internal DNS data.

</details>

---

### 16. What is the primary security risk posed by **open DNS resolvers**?

* [ ] Memory exhaustion
* [ ] Denial-of-Service amplification attacks
* [ ] Log overflow
* [ ] Database corruption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Denial-of-Service amplification attacks
💡 Open resolvers can be abused in reflection attacks to amplify traffic toward victims.

</details>

---

### 17. Which practice effectively restricts unauthorized DNS zone transfers in BIND?

* [ ] Disabling NTP
* [ ] Configuring `allow-transfer` in named.conf
* [ ] Increasing DNS TTL values
* [ ] Rotating log files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configuring `allow-transfer` in named.conf
💡 Proper access control prevents leakage of DNS infrastructure details.

</details>

---

### 18. What is the primary purpose of **log rotation** in Linux systems?

* [ ] Prevent indefinite growth of log files
* [ ] Refresh DNS records
* [ ] Synchronize system time
* [ ] Reset authentication tokens

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevent indefinite growth of log files
💡 Log rotation ensures disk availability and preserves historical logs for analysis.

</details>

---

### 19. What information does the command `ntpq -p` provide?

* [ ] Active Linux processes
* [ ] Peer status and synchronization state of NTP servers
* [ ] DNS zone transfer status
* [ ] ICMP latency results

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Peer status and synchronization state of NTP servers
💡 This command helps verify trusted time sources and detect anomalies.

</details>

---

### 20. Which scenario represents a **direct DNS security threat**?

* [ ] Forward lookup resolution
* [ ] Redundant zone files
* [ ] DNS spoofing
* [ ] Local DNS caching

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS spoofing
💡 DNS spoofing can redirect users to malicious sites and enable credential theft.

</details>

---

### 21. Why is NTP typically implemented over UDP instead of TCP?

* [ ] UDP is slower
* [ ] UDP provides encryption
* [ ] UDP is lightweight and connectionless
* [ ] TCP does not support time synchronization

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** UDP is lightweight and connectionless
💡 Minimal overhead is critical for accurate and efficient time synchronization.

</details>

---

### 22. Which DNSSEC mechanism directly ensures **data integrity** of DNS records?

* [ ] Timestamps
* [ ] DNS caching
* [ ] Digital signatures
* [ ] MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signatures
💡 Resource Record Signatures (RRSIG) verify that DNS data has not been altered.

</details>

---

### 23. What security risk can arise from **misconfigured or verbose BIND logging**?

* [ ] Buffer overflow
* [ ] Log injection and information disclosure
* [ ] Cross-site scripting
* [ ] CPU throttling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Log injection and information disclosure
💡 Excessive logs may expose internal network structure and be manipulated by attackers.

</details>

---

### 24. What is the primary risk of using **unauthenticated NTP sources**?

* [ ] File system corruption
* [ ] Time manipulation via man-in-the-middle attacks
* [ ] IP address duplication
* [ ] Disk fragmentation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Time manipulation via man-in-the-middle attacks
💡 Incorrect time can invalidate logs, certificates, and forensic timelines.

</details>

---

### 25. Which log analysis pattern best indicates a **brute-force authentication attack**?

* [ ] DNS TTL inconsistencies
* [ ] Repeated failed login attempts from a single source
* [ ] Frequent NTP stratum changes
* [ ] High CPU temperature readings

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Repeated failed login attempts from a single source
💡 This is a classic indicator used in SIEM and SOC monitoring.

</details>

---

### 26. What is the primary security purpose of **DNS Response Policy Zones (RPZ)**?

* [ ] Improve logging throughput
* [ ] Define firewall ACLs
* [ ] Block or modify responses for malicious domains
* [ ] Archive DNS traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Block or modify responses for malicious domains
💡 RPZ enables policy-based DNS filtering to mitigate malware and phishing.

</details>

---

### 27. Which BIND configuration directive disables recursive DNS queries?

* [ ] recursion off;
* [ ] no-recursion true;
* [ ] recursion no;
* [ ] allow-recursion none;

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** recursion off;
💡 Disabling recursion prevents abuse of authoritative servers in amplification attacks.

</details>

---

### 28. How can attackers exploit a **poorly secured NTP server**?

* [ ] DNS tunneling
* [ ] Reflection-based DDoS attacks
* [ ] Session hijacking
* [ ] Log poisoning

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reflection-based DDoS attacks
💡 NTP amplification attacks were historically used in large-scale DDoS campaigns.

</details>

---

### 29. In DNSSEC terminology, what is a **signed zone**?

* [ ] A zone with encrypted log entries
* [ ] A zone whose resource records are cryptographically signed
* [ ] A cached DNS response
* [ ] A segmented log buffer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A zone whose resource records are cryptographically signed
💡 Signing ensures authenticity and integrity of DNS data.

</details>

---

### 30. Why is **log tampering** considered a severe security threat?

* [ ] It increases log file size
* [ ] It corrupts system binaries
* [ ] It conceals attacker actions and disrupts forensic analysis
* [ ] It accelerates audit processes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It conceals attacker actions and disrupts forensic analysis
💡 Trustworthy logs are critical for detection, response, and legal proceedings.

</details>

---

## **Session 19 : Linux OS**

---

### 1. What does LDAP stand for?

* [ ] Local Directory Access Protocol
* [ ] Long Data Application Protocol
* [ ] List Directory Active Process
* [ ] Lightweight Directory Access Protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lightweight Directory Access Protocol
💡 LDAP is a protocol used to access and manage directory services over a network. It is “lightweight” because it is a simplified version of the older X.500 directory protocol.

</details>

---

### 2. What is the primary use of NIS in a networked environment?

* [ ] Managing email delivery
* [ ] Time synchronization
* [ ] IP address management
* [ ] Centralized user authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centralized user authentication
💡 NIS (Network Information Service) provides centralized authentication and user account management for UNIX/Linux networks, simplifying administration.

</details>

---

### 3. Apache HTTP Server is primarily used as a:

* [ ] Database engine
* [ ] File manager
* [ ] Web server
* [ ] Authentication server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Web server
💡 Apache serves HTTP requests and hosts websites. While it can integrate with authentication modules or database backends, its primary role is as a web server.

</details>

---

### 4. Which of the following best describes the function of a load balancer?

* [ ] A firewall tool
* [ ] A data encryption service
* [ ] A traffic distribution system
* [ ] A file system checker

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A traffic distribution system
💡 Load balancers distribute incoming network traffic across multiple servers to ensure availability and scalability.

</details>

---

### 5. Which port does LDAP typically use for unencrypted communication?

* [ ] 25
* [ ] 389
* [ ] 636
* [ ] 8080

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 389
💡 LDAP uses port 389 for standard (unencrypted) connections and port 636 for LDAPS (encrypted) connections.

</details>

---

### 6. Which tool is commonly used for clustering Apache servers to achieve high availability?

* [ ] MySQL
* [ ] Heartbeat
* [ ] NIS
* [ ] FTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Heartbeat
💡 Heartbeat is part of Linux-HA and monitors server nodes. It detects failures and enables failover between clustered Apache servers.

</details>

---

### 7. Which command is used to test LDAP connectivity in Linux?

* [ ] curl
* [ ] whoami
* [ ] netstat
* [ ] ldapsearch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ldapsearch
💡 The `ldapsearch` command queries LDAP directories to verify connectivity and retrieve entries.

</details>

---

### 8. A directory service like LDAP organizes information primarily into:

* [ ] SQL tables
* [ ] Object trees
* [ ] Hexadecimal arrays
* [ ] Packet frames

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Object trees
💡 LDAP stores directory entries in a hierarchical tree structure called a Directory Information Tree (DIT).

</details>

---

### 9. On a Linux client, which file defines the NIS domain settings?

* [ ] /etc/nis.conf
* [ ] /etc/defaultdomain
* [ ] /etc/nsswitch.conf
* [ ] /etc/hosts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/defaultdomain
💡 `/etc/defaultdomain` sets the NIS domain name for a client. `/etc/nsswitch.conf` controls which services provide system databases.

</details>

---

### 10. In an Apache cluster, session persistence (sticky sessions) ensures:

* [ ] Load balancing across firewalls
* [ ] Encrypting user data
* [ ] Keeping a user's session on the same server
* [ ] Updating cache files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Keeping a user's session on the same server
💡 Sticky sessions bind a user’s session to a specific server so session data remains consistent across requests.

</details>

---

### 11. Which protocol does NIS commonly use for transferring data?

* [ ] TCP
* [ ] UDP
* [ ] HTTP
* [ ] FTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** UDP
💡 NIS uses UDP for most queries due to lower overhead and simplicity, although TCP can be used for larger transfers.

</details>

---

### 12. What is the purpose of `slapd` in LDAP?

* [ ] DNS resolution
* [ ] Web interface
* [ ] LDAP daemon/server
* [ ] Firewall configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** LDAP daemon/server
💡 `slapd` is the standalone LDAP daemon that handles directory service requests.

</details>

---

### 13. Which tool is used for high availability in Apache clustering?

* [ ] mod_ssl
* [ ] pacemaker
* [ ] nftables
* [ ] systemd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** pacemaker
💡 Pacemaker monitors cluster resources and coordinates failover for Apache servers in a high availability setup.

</details>

---

### 14. In a round-robin DNS setup, which factor determines which server receives a request?

* [ ] CPU load
* [ ] Static IP rules
* [ ] DNS record rotation
* [ ] Client-side cookies

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS record rotation
💡 Round-robin DNS cycles through a list of IP addresses for a hostname, distributing requests across multiple servers.

</details>

---

### 15. What role does `nsswitch.conf` play in systems using LDAP or NIS?

* [ ] Sets user password expiration
* [ ] Loads web modules
* [ ] Configures which services provide system databases
* [ ] Creates backup files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configures which services provide system databases
💡 `nsswitch.conf` determines the order of lookup for user accounts, groups, hosts, and other system databases.

</details>

---

### 16. Which statement accurately describes load balancing?

* [ ] It increases memory on a server
* [ ] It distributes network traffic to multiple servers
* [ ] It is used to store backups
* [ ] It replaces DNS completely

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It distributes network traffic to multiple servers
💡 Load balancers enhance availability and performance by directing traffic across multiple backend servers.

</details>

---

### 17. In Apache, the function of `mod_proxy_balancer` is to:

* [ ] Encrypt web traffic
* [ ] Provide session cookies
* [ ] Balance HTTP requests among back-end servers
* [ ] Route emails to users

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Balance HTTP requests among back-end servers
💡 `mod_proxy_balancer` enables Apache to act as a reverse proxy, distributing requests to backend servers for scalability.

</details>

---

### 18. The LDAP Directory Information Tree (DIT) resembles:

* [ ] A SQL table
* [ ] A filesystem hierarchy
* [ ] A flat list
* [ ] A packet sniffer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A filesystem hierarchy
💡 LDAP DIT organizes entries hierarchically, similar to directories and files in a filesystem.

</details>

---

### 19. What does the NIS master server contain?

* [ ] All user login attempts
* [ ] The original NIS database files
* [ ] DNS configurations
* [ ] Apache log history

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The original NIS database files
💡 The NIS master server maintains the authoritative database, which is replicated to slave servers.

</details>

---

### 20. If a load balancer fails without failover, what is the most likely outcome?

* [ ] Users are redirected to backup DNS
* [ ] All server logs are deleted
* [ ] Web traffic halts
* [ ] Sessions are auto-recovered

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Web traffic halts
💡 Without failover, a failed load balancer interrupts traffic distribution, causing service downtime.

</details>

---

### 21. In LDAP, which object class defines standard user accounts?

* [ ] cn
* [ ] uid
* [ ] ldapUser
* [ ] inetOrgPerson

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** inetOrgPerson
💡 The `inetOrgPerson` object class represents user entries with common attributes like name, email, and password.

</details>

---

### 22. What is a major security concern when using NIS over an open network?

* [ ] Log overflow
* [ ] Password hashes are sent unencrypted
* [ ] Port exhaustion
* [ ] Data compression errors

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Password hashes are sent unencrypted
💡 NIS transmits credentials in plaintext or weakly hashed form, making it vulnerable to interception. Secure alternatives like LDAP over TLS are recommended.

</details>

---

### 23. In an LDAP schema, an OID (Object Identifier) uniquely represents:

* [ ] Operating system ID
* [ ] Organizational ID
* [ ] Object Identifier for attribute types
* [ ] Original Index Domain

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Object Identifier for attribute types
💡 OIDs uniquely identify attributes and object classes in LDAP schemas, ensuring consistency across directory implementations.

</details>

---

### 24. What is the impact of enabling sticky sessions on a load balancer?

* [ ] Clients can connect to multiple servers simultaneously
* [ ] Session is maintained with the same server
* [ ] Load is always distributed equally
* [ ] Encryption is enabled by default

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Session is maintained with the same server
💡 Sticky sessions ensure a user’s requests are routed to the same backend server, preserving session data. This can affect load distribution efficiency.

</details>

---

### 25. In Apache clustering, the “heartbeat” mechanism ensures:

* [ ] Disk replication between servers
* [ ] DNS propagation
* [ ] Server health and failover detection
* [ ] File system backup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server health and failover detection
💡 Heartbeat monitors server nodes in a cluster and triggers failover if a node becomes unresponsive, ensuring high availability.

</details>

---

### 26. The `ldapmodify` command is used to:

* [ ] List LDAP groups
* [ ] Connect to NIS domains
* [ ] Add or modify LDAP entries
* [ ] View session traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Add or modify LDAP entries
💡 `ldapmodify` allows administrators to create, update, or delete entries in an LDAP directory. It supports LDIF file input for bulk changes.

</details>

---

### 27. What is a potential downside of using round-robin DNS without health checks?

* [ ] Reduced encryption
* [ ] Increased DNSSEC conflicts
* [ ] Requests may be routed to down servers
* [ ] Log files cannot be generated

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Requests may be routed to down servers
💡 Round-robin DNS does not verify server health by default, so some clients may be directed to offline servers, causing service disruption.

</details>

---

### 28. How can LDAP traffic be secured effectively?

* [ ] Use TCP over port 21
* [ ] Use LDAPS over port 636
* [ ] Enable UDP mode
* [ ] Install a DNS firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use LDAPS over port 636
💡 LDAPS encrypts LDAP traffic using SSL/TLS on port 636, protecting credentials and sensitive directory data during transmission.

</details>

---

### 29. In a clustered Apache setup, which component tracks client-server mapping in sticky sessions?

* [ ] IP filter
* [ ] Session cookie
* [ ] Server-side firewall
* [ ] SSL certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Session cookie
💡 Sticky sessions use session cookies to consistently route a client to the same backend server, maintaining session state across requests.

</details>

---

### 30. Which best describes the role of a reverse proxy in load balancing?

* [ ] It prevents DoS attacks
* [ ] It decrypts user data
* [ ] It forwards client requests to backend servers
* [ ] It manages file system I/O

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It forwards client requests to backend servers
💡 A reverse proxy acts as an intermediary, routing incoming requests to multiple backend servers, balancing load and providing additional services like caching or SSL termination.

</details>

---

