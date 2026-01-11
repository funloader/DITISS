> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 05 


## **Session 6: Configuring DNS**

---

### 1. In an enterprise network, users access applications using human-readable names instead of IP addresses. Which service enables this abstraction?

* [ ] Dynamic Network System
* [ ] Digital Network Service
* [ ] Domain Network Service
* [ ] Domain Name System

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Domain Name System
💡 DNS translates human-readable domain names into machine-understandable IP addresses, forming a core Internet naming service.

</details>

---

### 2. When a user enters a URL in a browser, which primary function does DNS perform first?

* [ ] Encrypts the HTTP request
* [ ] Allocates an IP address dynamically
* [ ] Translates the domain name into an IP address
* [ ] Verifies server availability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Translates the domain name into an IP address
💡 DNS resolution is the first step before any TCP/IP communication can begin.

</details>

---

### 3. An administrator wants to create and manage zones and resource records on a Windows Server. Which tool should be used?

* [ ] Task Scheduler
* [ ] Group Policy Editor
* [ ] DNS Manager
* [ ] Server Monitor

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS Manager
💡 DNS Manager is the Microsoft MMC snap-in used to administer DNS servers, zones, and records.

</details>

---

### 4. Which DNS record type directly maps a hostname to an IPv4 address?

* [ ] MX
* [ ] TXT
* [ ] CNAME
* [ ] A

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A
💡 An **A (Address) record** resolves a domain name to an IPv4 address.

</details>

---

### 5. A firewall rule must allow standard DNS query traffic. Which port should be opened?

* [ ] 21
* [ ] 53
* [ ] 80
* [ ] 443

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 53
💡 DNS primarily uses **UDP port 53** for queries and **TCP 53** for zone transfers.

</details>

---

### 6. Which type of DNS server provides authoritative responses for publicly hosted domains?

* [ ] Caching-only
* [ ] Forwarder
* [ ] Authoritative
* [ ] Recursive resolver

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authoritative
💡 Authoritative DNS servers host original zone data and respond with final answers.

</details>

---

### 7. What is the technical term for converting a domain name into an IP address?

* [ ] Switching
* [ ] Routing
* [ ] Resolution
* [ ] Encapsulation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Resolution
💡 DNS name resolution is the systematic process of mapping names to IP addresses.

</details>

---

### 8. A security analyst investigates suspicious traffic originating from an IP address. Which DNS zone helps identify the associated domain name?

* [ ] Forward lookup zone
* [ ] Reverse lookup zone
* [ ] Stub zone
* [ ] Primary zone

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reverse lookup zone
💡 Reverse lookup zones use **PTR records** to map IP addresses back to domain names.

</details>

---

### 9. Which DNS record allows one domain name to act as an alias for another canonical domain?

* [ ] PTR
* [ ] NS
* [ ] SOA
* [ ] CNAME

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CNAME
💡 CNAME records provide domain name aliasing without duplicating A records.

</details>

---

### 10. In a distributed DNS infrastructure, which zone type contains only SOA, NS, and glue A records?

* [ ] Primary zone
* [ ] Secondary zone
* [ ] Stub zone
* [ ] Reverse zone

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Stub zone
💡 Stub zones reduce replication traffic while maintaining authoritative references.

</details>

---

### 11. What is the primary role of a secondary DNS server?

* [ ] Assign IP addresses
* [ ] Create authoritative records
* [ ] Provide redundancy for zone data
* [ ] Authenticate Active Directory users

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provide redundancy for zone data
💡 Secondary servers receive read-only copies via zone transfer to ensure availability.

</details>

---

### 12. Which DNS record identifies the authoritative name servers for a zone?

* [ ] MX
* [ ] SRV
* [ ] NS
* [ ] TXT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NS
💡 NS records define which servers are responsible for answering queries for a zone.

</details>

---

### 13. DNS scavenging is enabled in a Windows environment. What is its main purpose?

* [ ] Prevent cache poisoning
* [ ] Remove outdated dynamic records
* [ ] Encrypt DNS zones
* [ ] Detect malicious domains

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Remove outdated dynamic records
💡 Scavenging cleans stale records that could otherwise cause name resolution issues.

</details>

---

### 14. An organization wants DNS queries for a partner domain to be resolved by a specific DNS server. Which feature supports this requirement?

* [ ] Root hints
* [ ] Conditional forwarding
* [ ] Recursive lookup
* [ ] Stub resolution

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Conditional forwarding
💡 Conditional forwarders route queries for specific domains to designated servers.

</details>

---

### 15. What does the TTL value in a DNS record control?

* [ ] DNS query encryption strength
* [ ] Record priority
* [ ] Cache lifetime of the record
* [ ] Number of allowed queries

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Cache lifetime of the record
💡 TTL determines how long a resolver caches a record before re-querying.

</details>

---

### 16. Which Windows command-line utility allows interactive DNS query testing?

* [ ] tracert
* [ ] ping
* [ ] netstat
* [ ] nslookup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** nslookup
💡 nslookup directly queries DNS servers and inspects responses.

</details>

---

### 17. Where are standard DNS zone files stored on a Windows Server (non-AD integrated)?

* [ ] C:\DNS\Zones
* [ ] C:\Windows\System\Zones
* [ ] C:\Windows\System32\DNS
* [ ] C:\Program Files\DNS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** C:\Windows\System32\DNS
💡 File-based DNS zones are stored in this default directory.

</details>

---

### 18. Which DNS record specifies the mail servers responsible for receiving emails?

* [ ] A
* [ ] CNAME
* [ ] TXT
* [ ] MX

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MX
💡 MX records define mail routing priorities for a domain.

</details>

---

### 19. Which DNS security extension ensures data integrity and origin authentication?

* [ ] DHCP
* [ ] DNS Cache
* [ ] DNSSEC
* [ ] IPsec

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNSSEC
💡 DNSSEC uses cryptographic signatures to prevent spoofing and cache poisoning.

</details>

---

### 20. What is the primary purpose of a DNS zone transfer?

* [ ] Forward queries
* [ ] Synchronize zone data between servers
* [ ] Encrypt DNS traffic
* [ ] Flush resolver cache

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Synchronize zone data between servers
💡 Zone transfers replicate DNS zone data from primary to secondary servers.

</details>

---

### 21. How do dynamic DNS updates function in a Windows domain environment?

* [ ] Require manual administrator approval
* [ ] Automatically update records via clients
* [ ] Apply only to static IP hosts
* [ ] Encrypt all DNS records

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Automatically update records via clients
💡 Dynamic updates allow systems to register and refresh DNS records automatically.

</details>

---

### 22. Which DNS record controls zone versioning and triggers zone transfers?

* [ ] PTR
* [ ] SRV
* [ ] TXT
* [ ] SOA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SOA
💡 The SOA serial number determines when secondaries initiate zone transfers.

</details>

---

### 23. What is the primary purpose of SRV records in Active Directory environments?

* [ ] Email routing
* [ ] Service discovery for domain services
* [ ] Website redirection
* [ ] DNS authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Service discovery for domain services
💡 SRV records advertise services like LDAP, Kerberos, and Global Catalog.

</details>

---

### 24. A DNS zone is configured for “Secure dynamic updates only.” What is the implication?

* [ ] Manual updates only
* [ ] DHCP-only updates
* [ ] Authenticated clients can update records
* [ ] Replication is disabled

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticated clients can update records
💡 This setting prevents unauthorized DNS record modifications.

</details>

---

### 25. Where are AD-integrated DNS zones stored?

* [ ] Registry
* [ ] Text files
* [ ] Active Directory database
* [ ] WINS repository

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active Directory database
💡 AD-integrated zones leverage AD replication and security.

</details>

---

### 26. Which resolution method avoids querying root servers by using predefined servers?

* [ ] Iterative resolution
* [ ] Forwarding
* [ ] Recursive lookup
* [ ] Stub resolution

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forwarding
💡 Forwarders reduce external DNS traffic and improve performance.

</details>

---

### 27. How does a caching-only DNS server function?

* [ ] Maintains authoritative zones
* [ ] Stores query responses temporarily
* [ ] Redirects all queries
* [ ] Validates DNSSEC only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Stores query responses temporarily
💡 It improves efficiency without hosting zone data.

</details>

---

### 28. Which misconfiguration can cause DNS resolution failure even when the service is running?

* [ ] High CPU usage
* [ ] Missing NS records
* [ ] Low disk space
* [ ] Incorrect WINS settings

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Missing NS records
💡 Without proper NS records, authoritative resolution fails.

</details>

---

### 29. What is the function of the root hints file in Windows DNS?

* [ ] Encrypt DNS responses
* [ ] Store root server IP addresses
* [ ] Set TTL limits
* [ ] Authenticate DNS clients

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Store root server IP addresses
💡 Root hints allow DNS servers to locate root servers for iterative queries.

</details>

---

### 30. Which DNS zone type contains only minimal records for resolving a specific domain?

* [ ] Primary zone
* [ ] Reverse lookup zone
* [ ] Stub zone
* [ ] Conditional forwarding zone

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Stub zone
💡 Stub zones optimize resolution while minimizing data replication.

</details>

---

## **Session 7: Implement DHCP and IPAM**

---

### 1. In an enterprise network, hosts dynamically receive IP configuration without manual intervention. Which protocol enables this functionality?

* [ ] Domain Host Control Protocol
* [ ] Direct Host Control Program
* [ ] Dynamic Host Configuration Protocol
* [ ] Data Host Configuration Protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamic Host Configuration Protocol
💡 DHCP is a network management protocol that automatically assigns IP addresses and related network parameters to clients.

</details>

---

### 2. What is the primary operational role of a DHCP server in a LAN environment?

* [ ] Maintaining DNS zone files
* [ ] Automatically assigning IP addresses to clients
* [ ] Managing Active Directory user accounts
* [ ] Enforcing Group Policy Objects

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Automatically assigning IP addresses to clients
💡 DHCP eliminates manual IP configuration by leasing addresses and network parameters dynamically.

</details>

---

### 3. During the initial phase of IP acquisition, which device sends a DHCPDISCOVER message?

* [ ] DNS Server
* [ ] DHCP Server
* [ ] Client Device
* [ ] Core Router

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Client Device
💡 A client broadcasts DHCPDISCOVER to locate available DHCP servers on the network.

</details>

---

### 4. In DHCP terminology, what does a “lease” represent?

* [ ] A permanently assigned IP address
* [ ] A temporary IP address assignment for a defined duration
* [ ] A subnet mask configuration
* [ ] A MAC address authorization rule

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A temporary IP address assignment for a defined duration
💡 DHCP leases are time-bound, ensuring efficient reuse of IP addresses.

</details>

---

### 5. On which UDP port does a DHCP client initially send its request messages?

* [ ] 80
* [ ] 67
* [ ] 68
* [ ] 53

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 68
💡 DHCP clients use UDP port 68, while DHCP servers listen on UDP port 67.

</details>

---

### 6. What best describes a DHCP scope?

* [ ] A DNS namespace
* [ ] A defined IP address range with associated configuration parameters
* [ ] A domain-level security policy
* [ ] A NAT translation rule

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A defined IP address range with associated configuration parameters
💡 A scope specifies the pool of IP addresses and options available for lease.

</details>

---

### 7. Which of the following is NOT a valid DHCP message type?

* [ ] DHCPDISCOVER
* [ ] DHCPREQUEST
* [ ] DHCPDELETE
* [ ] DHCPACK

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DHCPDELETE
💡 DHCPDELETE is not defined in the DHCP protocol message set.

</details>

---

### 8. An administrator wants a specific server to always receive the same IP address via DHCP. What feature should be used?

* [ ] IP conflict detection
* [ ] DHCP reservation mapped to MAC address
* [ ] Exclusion range
* [ ] Split scope

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DHCP reservation mapped to MAC address
💡 Reservations ensure consistent IP assignment while retaining centralized DHCP control.

</details>

---

### 9. When a DHCP client detects that an offered IP address is already in use, which message does it send?

* [ ] DHCPACK
* [ ] DHCPDECLINE
* [ ] DHCPRELEASE
* [ ] DHCPINFORM

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DHCPDECLINE
💡 DHCPDECLINE informs the server that the offered IP address is invalid due to conflict.

</details>

---

### 10. Besides assigning an IP address, what essential configuration parameters does a DHCP server typically provide?

* [ ] Only the IP address
* [ ] DNS server, default gateway, and subnet mask
* [ ] File server paths
* [ ] Domain controller credentials

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS server, default gateway, and subnet mask
💡 These parameters are delivered via DHCP options to ensure full network connectivity.

</details>

---

### 11. Identify the correct sequence of the standard DHCP four-step handshake.

* [ ] Request → Offer → Discover → Acknowledge
* [ ] Discover → Offer → Request → Acknowledge
* [ ] Offer → Discover → Request → Acknowledge
* [ ] Discover → Request → Offer → Acknowledge

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Discover → Offer → Request → Acknowledge
💡 This DORA process governs dynamic IP address allocation.

</details>

---

### 12. What is the primary purpose of the DHCPINFORM message?

* [ ] To release the IP address
* [ ] To request additional configuration parameters
* [ ] To disable DHCP on the client
* [ ] To renew an expired lease

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To request additional configuration parameters
💡 DHCPINFORM is used when a client already has an IP but needs other options.

</details>

---

### 13. Which component enables DHCP communication across different IP subnets?

* [ ] DHCP Repeater
* [ ] DNS Forwarder
* [ ] DHCP Relay Agent
* [ ] IP Proxy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DHCP Relay Agent
💡 Relay agents forward DHCP broadcasts across routed networks.

</details>

---

### 14. What is the function of an exclusion range in a DHCP scope?

* [ ] Blocking unauthorized clients
* [ ] Reserving specific IP addresses from being leased
* [ ] Prioritizing critical hosts
* [ ] Filtering MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reserving specific IP addresses from being leased
💡 Exclusions prevent DHCP from assigning addresses used by static devices.

</details>

---

### 15. In a Windows DHCP server implementation, where is the DHCP database stored?

* [ ] dhcp.mdb
* [ ] dhcp.xml
* [ ] leases.txt
* [ ] dhcp.ini

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dhcp.mdb
💡 The DHCP database file stores lease and configuration information.

</details>

---

### 16. What is the default lease duration for a Windows DHCP scope?

* [ ] 12 hours
* [ ] 1 day
* [ ] 7 days
* [ ] 30 days

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 8 days (commonly approximated as 7 days in exam context)
💡 Windows DHCP defaults to an 8-day lease, often rounded to 7 days in exams.

</details>

---

### 17. Which PowerShell cmdlet is used to install the DHCP Server role?

* [ ] Install-WindowsFeature DHCP
* [ ] Add-WindowsFeature DHCP
* [ ] Enable-DHCPService
* [ ] Install-DHCPServer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Install-WindowsFeature DHCP
💡 This cmdlet installs the DHCP role on Windows Server systems.

</details>

---

### 18. What is the function of the DHCPACK message?

* [ ] Rejects the client request
* [ ] Confirms IP lease assignment
* [ ] Requests additional client information
* [ ] Terminates the lease

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Confirms IP lease assignment
💡 DHCPACK finalizes the IP assignment process.

</details>

---

### 19. What is the effect of running `ipconfig /release` on a Windows client?

* [ ] Clears the DNS resolver cache
* [ ] Releases the leased IP address to the DHCP server
* [ ] Forces lease renewal
* [ ] Disables the network interface

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Releases the leased IP address to the DHCP server
💡 This command relinquishes the current DHCP lease.

</details>

---

### 20. What is the purpose of DHCP scope options?

* [ ] Assigning static IPs
* [ ] Providing additional configuration like DNS and gateway
* [ ] Enforcing security policies
* [ ] Blocking unknown clients

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Providing additional configuration like DNS and gateway
💡 Scope options standardize network settings across clients.

</details>

---

### 21. What does DHCP failover primarily provide in enterprise environments?

* [ ] IP reassignment only
* [ ] High availability and load balancing
* [ ] Secure DHCP over VPN
* [ ] Traffic shaping

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** High availability and load balancing
💡 DHCP failover ensures continuous service during server outages.

</details>

---

### 22. In DHCP failover configuration, which mode allows both servers to actively share client load?

* [ ] Standby
* [ ] Hot Spare
* [ ] Load Sharing
* [ ] Mirroring

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Load Sharing
💡 Load Sharing distributes IP assignment requests between two active servers.

</details>

---

### 23. Which protocol is used for communication between DHCP failover partner servers?

* [ ] HTTPS
* [ ] TCP
* [ ] SNMP
* [ ] UDP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TCP
💡 DHCP failover communication relies on reliable TCP sessions.

</details>

---

### 24. What is meant by a “split scope” configuration?

* [ ] A scope handling IPv4 and IPv6
* [ ] A scope divided across multiple DHCP servers
* [ ] A scope shared between multiple subnets
* [ ] A scope containing only static IPs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A scope divided across multiple DHCP servers
💡 Split scope improves redundancy in environments without native failover.

</details>

---

### 25. Which event ID is logged when a DHCP server detects an IP address conflict?

* [ ] 1001
* [ ] 1014
* [ ] 1050
* [ ] 1007

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1007
💡 Event ID 1007 indicates address conflict detection.

</details>

---

### 26. In DHCP failover, what does the status “COMMUNICATION INTERRUPTED” indicate?

* [ ] Server reboot in progress
* [ ] Normal operational state
* [ ] Network or configuration issue between partners
* [ ] Both servers are synchronized

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network or configuration issue between partners
💡 This status signals loss of synchronization or connectivity.

</details>

---

### 27. What is the impact of configuring a very short DHCP lease duration?

* [ ] Improved network performance
* [ ] Reduced DHCP traffic
* [ ] Increased DHCP traffic and administrative overhead
* [ ] No noticeable impact

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Increased DHCP traffic and administrative overhead
💡 Frequent renewals increase broadcast traffic and server load.

</details>

---

### 28. How does DHCP typically detect IP address conflicts?

* [ ] Assigns the address regardless
* [ ] Logs a warning only
* [ ] Uses ARP probing before lease confirmation
* [ ] Automatically resolves conflicts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Uses ARP probing before lease confirmation
💡 Conflict detection relies on ARP checks to ensure uniqueness.

</details>

---

### 29. In IPv6 networking, what is the DHCP equivalent protocol?

* [ ] SLAAC
* [ ] DHCPv6
* [ ] Router Advertisement
* [ ] IP6Config

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DHCPv6
💡 DHCPv6 provides stateful configuration for IPv6 networks.

</details>

---

### 30. What is the primary purpose of DHCP Option 82?

* [ ] Indicating lease expiration
* [ ] Identifying client MAC address
* [ ] Providing relay agent information
* [ ] Defining static reservations

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Providing relay agent information
💡 Option 82 enhances security and tracking in relay-based DHCP deployments.

</details>

---
