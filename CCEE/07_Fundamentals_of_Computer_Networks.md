> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---
# 200 MCQ Set

---

### 1. In a PPP connection, which command correctly sets a username and password for authentication on a Cisco router?

* [ ] auth user
* [ ] username <name> password <pass>
* [ ] ppp user set
* [ ] set auth credentials

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** username <name> password <pass>
💡 This command defines a local username and password for PPP authentication. Other options are either non-existent or incorrect syntactically. PPP supports PAP and CHAP, both requiring locally defined credentials.

</details>

---

### 2. To create a GRE tunnel interface on a router, which command is used?

* [ ] interface gre
* [ ] interface tunnel <number>
* [ ] tunnel gre create
* [ ] create tunnel gre

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** interface tunnel <number>
💡 GRE tunnels are logical interfaces in routers. The `interface tunnel <number>` command initiates a tunnel configuration where source, destination, and other parameters are defined. “interface gre” is invalid syntax.

</details>

---

### 3. Which command specifies the remote endpoint IP address for a GRE tunnel?

* [ ] tunnel destination
* [ ] tunnel peer
* [ ] set destination ip
* [ ] remote endpoint ip

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** tunnel destination
💡 The `tunnel destination <IP>` command sets the remote endpoint for a GRE tunnel. Without this, the tunnel cannot establish a path. “tunnel peer” is not standard Cisco syntax.

</details>

---

### 4. What is a primary advantage of GRE tunnels compared to direct IP routing?

* [ ] They provide encryption
* [ ] They encapsulate multicast and routing protocols
* [ ] They reduce latency
* [ ] They compress packets

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They encapsulate multicast and routing protocols
💡 GRE tunnels encapsulate Layer 3 packets over IP, including multicast, IPv6, and routing protocols like OSPF and EIGRP. GRE does **not provide encryption**—IPsec is needed for that.

</details>

---

### 5. Which type of BGP session is established between routers in different autonomous systems?

* [ ] iBGP
* [ ] eBGP
* [ ] sBGP
* [ ] mBGP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** eBGP
💡 eBGP (external BGP) is used between different autonomous systems (AS). iBGP is for peers within the same AS. sBGP and mBGP are not standard terms.

</details>

---

### 6. On a Cisco router, which command starts the BGP process for a specific AS number?

* [ ] start bgp
* [ ] router bgp <AS number>
* [ ] set bgp process
* [ ] ip bgp enable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** router bgp <AS number>
💡 The `router bgp <AS>` command initiates the BGP routing process and allows configuration of neighbors, networks, and policies.

</details>

---

### 7. How is an eBGP neighbor defined on a router?

* [ ] bgp neighbor
* [ ] ip neighbor
* [ ] neighbor <IP> remote-as <AS>
* [ ] bgp-peer set

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** neighbor <IP> remote-as <AS>
💡 To form an eBGP session, the neighbor's IP and remote AS number must be configured. This is the standard syntax in Cisco IOS.

</details>

---

### 8. What does the `network` command in BGP achieve?

* [ ] Sets up BGP filters
* [ ] Advertises a network in BGP
* [ ] Creates BGP tunnels
* [ ] Shows BGP neighbors

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Advertises a network in BGP
💡 The `network <network> mask <mask>` command announces networks to BGP peers. It does not create tunnels or show neighbors.

</details>

---

### 9. Which command verifies the status of BGP sessions on a Cisco router?

* [ ] show ip route
* [ ] show ip bgp summary
* [ ] show ip ospf neighbor
* [ ] debug ip bgp updates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** show ip bgp summary
💡 This command displays BGP neighbor relationships, session states, and prefixes received. It is the standard verification command for BGP sessions.

</details>

---

### 10. For a BGP neighbor relationship to form successfully, what is required?

* [ ] Matching passwords
* [ ] Same autonomous system
* [ ] Defined remote-as and reachable IP
* [ ] Static route configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Defined remote-as and reachable IP
💡 A BGP session requires the neighbor's IP to be reachable and the remote AS correctly configured. Passwords are optional (for MD5), and the AS does **not** need to match in eBGP.

</details>

---

### 11. If CHAP authentication fails during a PPP connection attempt, what occurs?

* [ ] The connection is established without authentication
* [ ] The connection is dropped
* [ ] It falls back to PAP
* [ ] Traffic is encrypted instead

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The connection is dropped
💡 CHAP (Challenge Handshake Authentication Protocol) requires successful challenge-response verification. Failure causes the PPP session to terminate; it does **not** automatically fall back to PAP or enable encryption.

</details>

---

### 12. When configuring MLPPP on two physical serial interfaces, what is mandatory?

* [ ] They must be in the same VLAN
* [ ] Assign them to the same multilink group
* [ ] Configure NAT
* [ ] Use identical bandwidths only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Assign them to the same multilink group
💡 Multi-Link PPP (MLPPP) aggregates multiple physical links into a single logical link. Assigning interfaces to the same multilink group is essential; bandwidth matching is recommended but not strictly required.

</details>

---

### 13. Which command is used to verify active PPP authentication processes?

* [ ] show interfaces
* [ ] debug ppp authentication
* [ ] show ip protocols
* [ ] debug ip nat

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** debug ppp authentication
💡 This command actively monitors PPP authentication attempts (PAP/CHAP). `show interfaces` shows link status but not authentication specifics.

</details>

---

### 14. For a GRE tunnel, which command sets the IP address of the tunnel source interface?

* [ ] tunnel peer-ip
* [ ] tunnel origin
* [ ] tunnel source <interface/IP>
* [ ] ip tunnel local

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** tunnel source <interface/IP>
💡 The `tunnel source` command specifies which local interface or IP address initiates GRE encapsulation. Without it, the tunnel cannot establish correctly.

</details>

---

### 15. In PPPoE, what configuration step immediately follows successful authentication?

* [ ] IP address negotiation
* [ ] GRE tunnel formation
* [ ] Static routing
* [ ] OSPF neighbor adjacency

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IP address negotiation
💡 After PPPoE authentication, the client negotiates an IP address (via IPCP). GRE or routing protocols are configured subsequently.

</details>

---

### 16. Over a GRE tunnel, which type of routing protocol can be used?

* [ ] Only static routing
* [ ] Any dynamic routing protocol
* [ ] BGP only
* [ ] RIP only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Any dynamic routing protocol
💡 GRE tunnels provide a virtual point-to-point link over IP. Protocols like OSPF, EIGRP, RIP, or BGP can operate over the tunnel as if it were a physical interface.

</details>

---

### 17. In eBGP, if the remote neighbor IP is unreachable, what happens?

* [ ] BGP will try other interfaces
* [ ] The session remains idle
* [ ] A static route is installed automatically
* [ ] The connection defaults to iBGP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The session remains idle
💡 eBGP requires TCP connectivity to the configured neighbor. If the neighbor is unreachable, the session cannot establish and remains in Idle state.

</details>

---

### 18. Which command advertises the network 10.0.0.0/24 in BGP?

* [ ] network 10.0.0.0 255.255.255.0
* [ ] advertise 10.0.0.0/24
* [ ] network 10.0.0.0 mask 255.255.255.0
* [ ] ip bgp advertise 10.0.0.0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** network 10.0.0.0 mask 255.255.255.0
💡 Cisco IOS requires the full `network <network> mask <mask>` syntax for BGP advertisement. Other forms are invalid or unsupported.

</details>

---

### 19. Which condition can cause a GRE tunnel to remain in a down state?

* [ ] Tunnel source and destination in the same subnet
* [ ] MTU mismatch
* [ ] Inactive routing protocol
* [ ] Tunnel destination is unreachable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tunnel destination is unreachable
💡 GRE tunnels require IP reachability between source and destination. MTU mismatch or inactive routing may degrade performance, but the tunnel interface only stays down if the destination is unreachable.

</details>

---

### 20. What does SDN stand for?

* [ ] Software-Directed Network
* [ ] Software-Defined Networking
* [ ] Standard Distributed Network
* [ ] Secure Data Network

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Software-Defined Networking
💡 SDN abstracts network control from forwarding, enabling programmable networks. Other options are incorrect expansions.

</details>

---

### 21. What is the primary goal of SDN?

* [ ] Increase network cabling
* [ ] Decouple the control plane from the data plane
* [ ] Merge physical and virtual devices
* [ ] Reduce CPU usage on routers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Decouple the control plane from the data plane
💡 SDN separates decision-making (control plane) from forwarding (data plane), allowing centralized management and automation.

</details>

---

### 22. In SDN, what is the primary function of the controller?

* [ ] Provides DNS services
* [ ] Makes forwarding decisions
* [ ] Transmits Ethernet frames
* [ ] Manages physical cable connections

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Makes forwarding decisions
💡 The SDN controller acts as the “brain,” computing optimal paths and programming the data plane devices. It does **not physically transmit packets** or manage cabling directly.

</details>

---

### 23. Which of the following is NOT a layer in the standard SDN architecture?

* [ ] Infrastructure Layer
* [ ] Control Layer
* [ ] Application Layer
* [ ] Transport Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Transport Layer
💡 SDN architecture typically includes the **Application Layer**, **Control Layer**, and **Infrastructure Layer**. Transport Layer is part of the TCP/IP stack, not SDN layering.

</details>

---

### 24. What does the southbound interface in SDN connect?

* [ ] Applications to hardware
* [ ] Control plane to data plane
* [ ] Cloud to edge
* [ ] End users to switches

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Control plane to data plane
💡 Southbound APIs (e.g., OpenFlow, NetConf) allow the controller to communicate instructions to network devices for flow handling.

</details>

---

### 25. Which of the following is a commonly used southbound protocol in SDN?

* [ ] HTTPS
* [ ] OpenFlow
* [ ] SSH
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OpenFlow
💡 OpenFlow is the most widely adopted southbound protocol in SDN, allowing direct control over the data plane. SNMP is monitoring, and HTTPS/SSH are transport protocols.

</details>

---

### 26. In SDN, which layer typically runs network applications?

* [ ] Data Plane
* [ ] Control Plane
* [ ] Application Plane
* [ ] Physical Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Application Plane
💡 The Application Plane hosts business and network applications (firewall, load balancing, monitoring) that interact with the controller via northbound APIs.

</details>

---

### 27. Which SDN feature best supports scalability in large networks?

* [ ] Enables faster optical switching
* [ ] Simplifies management of large-scale networks
* [ ] Eliminates network redundancy
* [ ] Removes physical bandwidth limits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Simplifies management of large-scale networks
💡 Centralized control allows consistent policy enforcement and dynamic provisioning across hundreds or thousands of devices, greatly improving scalability.

</details>

---

### 28. How is SDN used in data centers to optimize traffic flows?

* [ ] Increase cable lengths
* [ ] Reduce air conditioning
* [ ] Dynamically manage traffic flows
* [ ] Power off idle servers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamically manage traffic flows
💡 SDN can reroute traffic in real-time to avoid congestion, prioritize critical flows, and balance loads without manual reconfiguration.

</details>

---

### 29. What is a core function of the SDN control plane?

* [ ] Transmitting packets
* [ ] Monitoring power usage
* [ ] Determining network paths
* [ ] Configuring BIOS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Determining network paths
💡 The control plane computes routes and policies for forwarding devices. Packet transmission occurs in the data plane, not the control plane.

</details>

---

### 30. Which SDN layer is responsible for forwarding packets?

* [ ] Application Layer
* [ ] Control Layer
* [ ] Infrastructure Layer
* [ ] Hypervisor Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Infrastructure Layer
💡 The Infrastructure Layer (data plane) physically or virtually forwards packets according to flow rules set by the controller.

</details>

---

### 31. What does “northbound API” in SDN refer to?

* [ ] Communication between routers
* [ ] Interface between control and data planes
* [ ] Interface between controller and applications
* [ ] ISP interconnection protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Interface between controller and applications
💡 Northbound APIs (like REST or gRPC) allow applications to request network services and report telemetry from the controller.

</details>

---

### 32. Why is SDN considered more agile than traditional networks?

* [ ] It uses larger routers
* [ ] It supports automatic cable patching
* [ ] Network configurations are centrally programmable
* [ ] It runs on layer 1 switches only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network configurations are centrally programmable
💡 Centralized programmability allows rapid policy deployment, automatic adjustments, and dynamic network reconfiguration without manual intervention.

</details>

---

### 33. How does SDN improve reliability?

* [ ] Disables redundant paths
* [ ] Allows faster failure detection and rerouting
* [ ] Reduces MTBF of hardware
* [ ] Prevents software updates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Allows faster failure detection and rerouting
💡 The controller can detect link/device failures and dynamically update forwarding rules to maintain network service continuity.

</details>

---

### 34. Which method helps maintain configuration consistency in SDN deployments?

* [ ] CLI access
* [ ] Manual backups
* [ ] Configuration templates and version control
* [ ] Random reboots

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configuration templates and version control
💡 Using standardized templates and version control ensures consistent deployment across controllers and switches, minimizing errors.

</details>

---

### 35. In SDN, access control violations occur when:

* [ ] A switch overheats
* [ ] Data plane devices run out of memory
* [ ] Unauthorized entities gain access to control interfaces
* [ ] Users unplug cables

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Unauthorized entities gain access to control interfaces
💡 Since the controller centrally manages the network, unauthorized access can compromise security and control across the network.

</details>

---

### 36. Why is configuration management important in SDN?

* [ ] To monitor fiber optics
* [ ] To ensure consistent behavior across controllers
* [ ] To detect network topology changes
* [ ] To prevent IP addressing conflicts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To ensure consistent behavior across controllers
💡 Proper configuration management avoids inconsistent policy application and ensures predictable network operation.

</details>

---

### 37. Which of the following is considered a northbound protocol?

* [ ] REST API
* [ ] OpenFlow
* [ ] BGP
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** REST API
💡 Northbound APIs like REST allow applications to communicate with SDN controllers. OpenFlow is southbound, BGP is routing, SNMP is monitoring.

</details>

---

### 38. A major challenge in adopting SDN in traditional networks is:

* [ ] Too many wireless access points
* [ ] Incompatibility with Ethernet
* [ ] Integration with legacy infrastructure
* [ ] Overreliance on cloud storage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Integration with legacy infrastructure
💡 Many networks have legacy devices not compatible with SDN protocols. Migrating to SDN requires careful integration planning.

</details>

---

### 39. Which is a significant security concern in SDN environments?

* [ ] Lack of routing tables
* [ ] Limited bandwidth
* [ ] Single point of failure at the controller
* [ ] Excessive copper cabling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Single point of failure at the controller
💡 The controller is central to network operation. If compromised or unavailable, the entire network could be impacted. Redundancy and clustering mitigate this risk.

</details>

---

### 40. In scalable SDN designs for ISPs, how are policies typically applied?

* [ ] Locally at each router
* [ ] Manually at every switch
* [ ] Centrally via the controller
* [ ] Through client-side scripts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centrally via the controller
💡 Centralized policy deployment ensures consistency, scalability, and easier maintenance compared to configuring individual devices manually.

</details>

---

Great! Let’s continue with **Questions 22–40**, covering **intermediate and difficult SDN topics**. I’ll ensure **scenario/application focus, single correct answers, and professional CCEE-level rigor**.

---

### 22. In SDN, what is the primary function of the controller?

* [ ] Provides DNS services
* [ ] Makes forwarding decisions
* [ ] Transmits Ethernet frames
* [ ] Manages physical cable connections

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Makes forwarding decisions
💡 The SDN controller acts as the “brain,” computing optimal paths and programming the data plane devices. It does **not physically transmit packets** or manage cabling directly.

</details>

---

### 23. Which of the following is NOT a layer in the standard SDN architecture?

* [ ] Infrastructure Layer
* [ ] Control Layer
* [ ] Application Layer
* [ ] Transport Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Transport Layer
💡 SDN architecture typically includes the **Application Layer**, **Control Layer**, and **Infrastructure Layer**. Transport Layer is part of the TCP/IP stack, not SDN layering.

</details>

---

### 24. What does the southbound interface in SDN connect?

* [ ] Applications to hardware
* [ ] Control plane to data plane
* [ ] Cloud to edge
* [ ] End users to switches

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Control plane to data plane
💡 Southbound APIs (e.g., OpenFlow, NetConf) allow the controller to communicate instructions to network devices for flow handling.

</details>

---

### 25. Which of the following is a commonly used southbound protocol in SDN?

* [ ] HTTPS
* [ ] OpenFlow
* [ ] SSH
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OpenFlow
💡 OpenFlow is the most widely adopted southbound protocol in SDN, allowing direct control over the data plane. SNMP is monitoring, and HTTPS/SSH are transport protocols.

</details>

---

### 26. In SDN, which layer typically runs network applications?

* [ ] Data Plane
* [ ] Control Plane
* [ ] Application Plane
* [ ] Physical Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Application Plane
💡 The Application Plane hosts business and network applications (firewall, load balancing, monitoring) that interact with the controller via northbound APIs.

</details>

---

### 27. Which SDN feature best supports scalability in large networks?

* [ ] Enables faster optical switching
* [ ] Simplifies management of large-scale networks
* [ ] Eliminates network redundancy
* [ ] Removes physical bandwidth limits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Simplifies management of large-scale networks
💡 Centralized control allows consistent policy enforcement and dynamic provisioning across hundreds or thousands of devices, greatly improving scalability.

</details>

---

### 28. How is SDN used in data centers to optimize traffic flows?

* [ ] Increase cable lengths
* [ ] Reduce air conditioning
* [ ] Dynamically manage traffic flows
* [ ] Power off idle servers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamically manage traffic flows
💡 SDN can reroute traffic in real-time to avoid congestion, prioritize critical flows, and balance loads without manual reconfiguration.

</details>

---

### 29. What is a core function of the SDN control plane?

* [ ] Transmitting packets
* [ ] Monitoring power usage
* [ ] Determining network paths
* [ ] Configuring BIOS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Determining network paths
💡 The control plane computes routes and policies for forwarding devices. Packet transmission occurs in the data plane, not the control plane.

</details>

---

### 30. Which SDN layer is responsible for forwarding packets?

* [ ] Application Layer
* [ ] Control Layer
* [ ] Infrastructure Layer
* [ ] Hypervisor Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Infrastructure Layer
💡 The Infrastructure Layer (data plane) physically or virtually forwards packets according to flow rules set by the controller.

</details>

---

### 31. What does “northbound API” in SDN refer to?

* [ ] Communication between routers
* [ ] Interface between control and data planes
* [ ] Interface between controller and applications
* [ ] ISP interconnection protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Interface between controller and applications
💡 Northbound APIs (like REST or gRPC) allow applications to request network services and report telemetry from the controller.

</details>

---

### 32. Why is SDN considered more agile than traditional networks?

* [ ] It uses larger routers
* [ ] It supports automatic cable patching
* [ ] Network configurations are centrally programmable
* [ ] It runs on layer 1 switches only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network configurations are centrally programmable
💡 Centralized programmability allows rapid policy deployment, automatic adjustments, and dynamic network reconfiguration without manual intervention.

</details>

---

### 33. How does SDN improve reliability?

* [ ] Disables redundant paths
* [ ] Allows faster failure detection and rerouting
* [ ] Reduces MTBF of hardware
* [ ] Prevents software updates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Allows faster failure detection and rerouting
💡 The controller can detect link/device failures and dynamically update forwarding rules to maintain network service continuity.

</details>

---

### 34. Which method helps maintain configuration consistency in SDN deployments?

* [ ] CLI access
* [ ] Manual backups
* [ ] Configuration templates and version control
* [ ] Random reboots

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configuration templates and version control
💡 Using standardized templates and version control ensures consistent deployment across controllers and switches, minimizing errors.

</details>

---

### 35. In SDN, access control violations occur when:

* [ ] A switch overheats
* [ ] Data plane devices run out of memory
* [ ] Unauthorized entities gain access to control interfaces
* [ ] Users unplug cables

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Unauthorized entities gain access to control interfaces
💡 Since the controller centrally manages the network, unauthorized access can compromise security and control across the network.

</details>

---

### 36. Why is configuration management important in SDN?

* [ ] To monitor fiber optics
* [ ] To ensure consistent behavior across controllers
* [ ] To detect network topology changes
* [ ] To prevent IP addressing conflicts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To ensure consistent behavior across controllers
💡 Proper configuration management avoids inconsistent policy application and ensures predictable network operation.

</details>

---

### 37. Which of the following is considered a northbound protocol?

* [ ] REST API
* [ ] OpenFlow
* [ ] BGP
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** REST API
💡 Northbound APIs like REST allow applications to communicate with SDN controllers. OpenFlow is southbound, BGP is routing, SNMP is monitoring.

</details>

---

### 38. A major challenge in adopting SDN in traditional networks is:

* [ ] Too many wireless access points
* [ ] Incompatibility with Ethernet
* [ ] Integration with legacy infrastructure
* [ ] Overreliance on cloud storage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Integration with legacy infrastructure
💡 Many networks have legacy devices not compatible with SDN protocols. Migrating to SDN requires careful integration planning.

</details>

---

### 39. Which is a significant security concern in SDN environments?

* [ ] Lack of routing tables
* [ ] Limited bandwidth
* [ ] Single point of failure at the controller
* [ ] Excessive copper cabling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Single point of failure at the controller
💡 The controller is central to network operation. If compromised or unavailable, the entire network could be impacted. Redundancy and clustering mitigate this risk.

</details>

---

### 40. In scalable SDN designs for ISPs, how are policies typically applied?

* [ ] Locally at each router
* [ ] Manually at every switch
* [ ] Centrally via the controller
* [ ] Through client-side scripts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centrally via the controller
💡 Centralized policy deployment ensures consistency, scalability, and easier maintenance compared to configuring individual devices manually.

</details>

---

### 41. Which consistency issue can arise when multiple SDN controllers are deployed?

* [ ] MAC address conflicts
* [ ] Topology loops
* [ ] State synchronization delays
* [ ] VLAN overlaps

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** State synchronization delays
💡 In multi-controller deployments, controllers must synchronize network state. Delays can cause inconsistent flow rules and policy violations.

</details>

---

### 42. Which metric best evaluates SDN reliability?

* [ ] Number of VLANs configured
* [ ] Controller uptime and failover response time
* [ ] Cable resistance level
* [ ] DHCP lease time

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Controller uptime and failover response time
💡 Reliability depends on controller availability and how quickly failover occurs to maintain network operations.

</details>

---

### 43. Which of the following is considered an opportunity of SDN?

* [ ] Centralized security policy enforcement
* [ ] Dependence on vendor-specific CLI
* [ ] Manual network provisioning
* [ ] Higher licensing costs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centralized security policy enforcement
💡 SDN allows security policies to be applied consistently across the network from a central controller, enhancing protection and reducing human error.

</details>

---

### 44. Which SDN mechanism enables automated service deployment in large data centers?

* [ ] Static routing
* [ ] Service chaining
* [ ] Port mirroring
* [ ] NAT overload

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Service chaining
💡 Service chaining allows traffic to flow through a sequence of virtual network functions (firewall, load balancer, DPI) automatically, supporting large-scale deployments.

</details>

---

### 45. What can lead to inconsistent configurations across SDN devices?

* [ ] Use of OpenFlow
* [ ] Centralized policy enforcement
* [ ] Uncoordinated controller updates
* [ ] Uniform configuration templates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Uncoordinated controller updates
💡 Multiple controllers that update flows independently without coordination can create inconsistent states across devices.

</details>

---

### 46. Which controller architecture provides better fault tolerance in SDN?

* [ ] Monolithic controller
* [ ] Centralized-only controller
* [ ] Distributed or clustered controller
* [ ] Isolated per-device controller

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Distributed or clustered controller
💡 Distributed or clustered controllers provide redundancy and failover capabilities, reducing the impact of a single controller failure.

</details>

---

### 47. How does intent-based networking in SDN differ from traditional approaches?

* [ ] It uses hardware-specific instructions
* [ ] It focuses on user goals rather than configuration commands
* [ ] It eliminates the need for controllers
* [ ] It avoids the application layer altogether

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It focuses on user goals rather than configuration commands
💡 Intent-based networking allows administrators to specify high-level objectives, and the controller translates them into low-level device configurations.

</details>

---

### 48. What is virtual networking primarily used for?

* [ ] Hardware replacement
* [ ] Simplifying cabling
* [ ] Creating logical networks independent of physical devices
* [ ] Increasing CPU speed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Creating logical networks independent of physical devices
💡 Virtual networking abstracts network resources, enabling multiple isolated logical networks over the same physical infrastructure.

</details>

---

### 49. Which component enables virtual networking within virtual machines?

* [ ] Physical router
* [ ] Hypervisor
* [ ] Monitor
* [ ] Firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hypervisor
💡 The hypervisor provides virtual switching and network interface abstraction, allowing VMs to communicate over virtual networks.

</details>

---

### 50. A virtual switch (vSwitch) primarily operates at which OSI layer?

* [ ] Layer 1
* [ ] Layer 2
* [ ] Layer 3
* [ ] Layer 4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Layer 2
💡 vSwitches forward frames based on MAC addresses, performing switching functions equivalent to a physical Layer 2 switch.

</details>

---

### 51. Which technology allows multiple virtual networks to coexist on the same physical infrastructure?

* [ ] NAT
* [ ] VLAN
* [ ] SSD
* [ ] BIOS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLAN
💡 VLANs (and overlays like VXLAN) isolate traffic between multiple virtual networks while sharing the same physical infrastructure.

</details>

---

### 52. What does VNIC stand for?

* [ ] Virtual Network Internet Controller
* [ ] Virtual NIC (Network Interface Card)
* [ ] Variable Network Interface Code
* [ ] Virtualized Network Internal Configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual NIC (Network Interface Card)
💡 VNIC is a software abstraction of a physical network interface assigned to a VM or container for network connectivity.

</details>

---

### 53. Which is a key benefit of virtual networking?

* [ ] Requires more physical ports
* [ ] Lower packet forwarding speed
* [ ] Easier network provisioning
* [ ] Limits scalability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Easier network provisioning
💡 Virtual networking enables rapid deployment of network resources without requiring physical hardware changes, enhancing agility and scalability.

</details>

---

### 54. In a virtualized environment, what connects virtual machines to the network?

* [ ] External firewall
* [ ] Router-only interface
* [ ] Virtual switch
* [ ] DNS server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual switch
💡 A virtual switch operates like a physical switch, connecting multiple VMs and forwarding traffic between them and the external network.

</details>

---

### 55. What is a common use case of Network Access Control (NAC)?

* [ ] Encrypting data at rest
* [ ] Granting network access based on device compliance
* [ ] Virtual machine backup
* [ ] Blocking emails

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Granting network access based on device compliance
💡 NAC enforces security policies by allowing only compliant devices to connect, mitigating security risks in virtual and physical networks.

</details>

---

### 56. Virtual Customer Edge (vCE) primarily benefits which scenario?

* [ ] Wireless access points
* [ ] Service providers offering multi-tenant services
* [ ] IoT sensors
* [ ] Printer configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Service providers offering multi-tenant services
💡 vCE virtualizes customer edge functions, enabling ISPs to provision services for multiple tenants efficiently without physical CPE devices.

</details>

---

### 57. In virtual networking, tunneling is used to:

* [ ] Detect malware
* [ ] Encrypt console output
* [ ] Transport virtual networks over physical networks
* [ ] Prevent IP address duplication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Transport virtual networks over physical networks
💡 GRE, VXLAN, or other tunnels encapsulate traffic to extend virtual networks over existing Layer 3 infrastructures.

</details>

---

### 58. One key optimization virtual networking brings to data centers is:

* [ ] Increases cooling requirements
* [ ] Adds more physical switches
* [ ] Reduces cable clutter and improves scalability
* [ ] Requires static routing only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduces cable clutter and improves scalability
💡 Virtual networking abstracts physical topology, reducing cabling complexity and enabling scalable provisioning of logical networks.

</details>

---

### 59. VXLAN is used in virtual networks to:

* [ ] Enhance DNS resolution
* [ ] Extend Layer 2 networks over Layer 3 infrastructure
* [ ] Encrypt router interfaces
* [ ] Block unauthorized MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Extend Layer 2 networks over Layer 3 infrastructure
💡 VXLAN encapsulates Layer 2 frames into UDP packets, allowing scalable tenant networks across routed infrastructure.

</details>

---

### 60. What is typically used to enforce network policies in a virtualized network?

* [ ] BIOS
* [ ] Virtual firewall
* [ ] Storage controller
* [ ] Terminal emulator

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual firewall
💡 Virtual firewalls provide security enforcement at the virtual network level, applying policies to VMs and segments without additional physical hardware.

</details>

---

### 61. What is a significant security challenge in virtual networking?

* [ ] Cable theft
* [ ] Increased power usage
* [ ] Lateral movement between virtual machines
* [ ] BIOS firmware incompatibility

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lateral movement between virtual machines
💡 In virtualized environments, malware or attackers can move laterally across VMs if segmentation or security policies are insufficient, making this a key security concern.

</details>

---

### 62. In a highly virtualized data center, which factor most influences network performance?

* [ ] Cable thickness
* [ ] Number of USB ports
* [ ] vSwitch throughput and latency
* [ ] RAM type

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** vSwitch throughput and latency
💡 The performance of virtual networks depends on the efficiency of virtual switches and their ability to handle packet forwarding between VMs.

</details>

---

### 63. What is a key characteristic of overlay networks in virtual networking?

* [ ] They are only physical paths
* [ ] Use VLAN IDs directly
* [ ] Abstract physical topology using encapsulated tunnels
* [ ] Require direct fiber interconnects

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Abstract physical topology using encapsulated tunnels
💡 Overlay networks (VXLAN, GRE) decouple logical network topology from physical infrastructure, encapsulating packets for transport.

</details>

---

### 64. In Virtual Customer Edge (vCE) design, control plane scalability is often achieved using:

* [ ] SNMP traps
* [ ] BGP with route reflectors
* [ ] Telnet scripting
* [ ] HTTP-based routing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** BGP with route reflectors
💡 Route reflectors reduce full-mesh BGP requirements, allowing scalable distribution of routing information in vCE deployments.

</details>

---

### 65. Which method allows SDN controllers to manage virtual networks dynamically?

* [ ] Static port forwarding
* [ ] Packet mirroring
* [ ] OpenFlow or NetConf APIs
* [ ] Manual CLI commands

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OpenFlow or NetConf APIs
💡 Controllers use southbound APIs to dynamically configure virtual networks and apply flow rules without manual intervention.

</details>

---

### 66. What potential issue arises from excessive virtual machine sprawl?

* [ ] Faster routing updates
* [ ] Simplified access control
* [ ] Increased attack surface and configuration complexity
* [ ] Redundant DHCP assignments

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Increased attack surface and configuration complexity
💡 Too many unmanaged VMs increase security risk and make network management and policy enforcement more complex.

</details>

---

### 67. In virtual networking, what is the role of NFV (Network Functions Virtualization)?

* [ ] Replace DNS with IPFS
* [ ] Use physical firewalls only
* [ ] Virtualize and deploy network services like firewalls or load balancers
* [ ] Standardize cable types

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtualize and deploy network services like firewalls or load balancers
💡 NFV allows traditional network functions to run as software on commodity hardware, enabling dynamic deployment and scaling.

</details>

---

### 68. What is a drawback of overlay network encapsulation like VXLAN?

* [ ] Increased bandwidth
* [ ] Reduced VLAN capacity
* [ ] Header overhead leading to MTU issues
* [ ] Incompatible with IPv6

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Header overhead leading to MTU issues
💡 VXLAN adds a 50-byte header per frame, which may require MTU adjustments to avoid fragmentation across physical networks.

</details>

---

### 69. In cloud environments, how does virtual networking enable agility?

* [ ] By reducing HTTP sessions
* [ ] Through dynamic provisioning and automated scaling of network resources
* [ ] By minimizing hypervisor usage
* [ ] Using static subnetting policies

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Through dynamic provisioning and automated scaling of network resources
💡 Virtual networks allow rapid creation, modification, and scaling of logical networks without touching physical infrastructure, improving agility.

</details>

---

### 70. What does OpenFlow primarily enable in a network?

* [ ] Packet encryption
* [ ] Control and data plane integration
* [ ] Control and data plane separation
* [ ] Physical router management

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Control and data plane separation
💡 OpenFlow allows the controller to program flow rules into switches, separating network intelligence from packet forwarding.

</details>

---

### 71. Which organization initially developed OpenFlow?

* [ ] Cisco Systems
* [ ] Stanford University
* [ ] IEEE
* [ ] Linux Foundation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Stanford University
💡 OpenFlow was developed at Stanford as part of the Clean Slate program to enable research in programmable networks.

</details>

---

### 72. In traditional networks, where does the control plane reside?

* [ ] In a centralized server
* [ ] Inside each individual network device
* [ ] On the cloud
* [ ] In virtual switches only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Inside each individual network device
💡 Traditional routers/switches make forwarding decisions locally (distributed control), unlike SDN where the control plane is centralized.

</details>

---

### 73. The data plane is mainly responsible for:

* [ ] Managing routing policies
* [ ] Forwarding packets
* [ ] Handling administrative tasks
* [ ] Encrypting user data

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forwarding packets
💡 The data plane forwards packets based on rules defined by the control plane, without making routing decisions itself.

</details>

---

### 74. The basic unit of forwarding in OpenFlow is:

* [ ] Routing table
* [ ] ARP table
* [ ] Flow table
* [ ] Link-state database

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Flow table
💡 Flow tables store match-action rules for packets. The controller programs flow entries to define how traffic is handled by switches.

</details>

---

### 75. In OpenFlow, which plane makes decisions about where traffic should be sent?

* [ ] Data plane
* [ ] Forwarding plane
* [ ] Control plane
* [ ] Management plane

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Control plane
💡 The controller (control plane) decides routing paths and policies, while the data plane forwards packets accordingly.

</details>

---

### 76. How is a switch identified to the controller in OpenFlow?

* [ ] Hostname
* [ ] IP address
* [ ] Datapath ID
* [ ] MAC address only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Datapath ID
💡 Each OpenFlow switch has a unique 64-bit Datapath ID, used by the controller for identification and management.

</details>

---

### 77. What is the main benefit of using OpenFlow in enterprise networks?

* [ ] Lower IP range consumption
* [ ] Simplified policy enforcement and automation
* [ ] Replacement of wireless access points
* [ ] Elimination of data encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Simplified policy enforcement and automation
💡 OpenFlow enables centralized network programming, automating flow configuration and simplifying enforcement of policies.

</details>

---

### 78. In SDN, what acts as the "brain" of the network?

* [ ] Data plane
* [ ] Firewall
* [ ] Controller
* [ ] Switch ASIC

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Controller
💡 The controller makes decisions, manages flow rules, and programs the data plane—centralizing intelligence in the network.

</details>

---

### 79. What is the purpose of flow timeout values in OpenFlow?

* [ ] Measure switch temperature
* [ ] Limit memory allocation
* [ ] Remove idle or hard flows after specific periods
* [ ] Schedule DNS updates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Remove idle or hard flows after specific periods
💡 Timeouts prevent stale flows from consuming memory, and ensure the switch adapts to network changes dynamically.

</details>

---

### 80. What communication channel does OpenFlow typically use between switches and controllers?

* [ ] Serial link
* [ ] Out-of-band management
* [ ] Secure TCP connection
* [ ] HDMI port

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Secure TCP connection
💡 OpenFlow uses TCP (commonly port 6633 or 6653) to establish a secure connection between the switch and controller, ensuring reliable communication.

</details>

---

### 81. What role does OpenDaylight primarily play in a Software Defined Networking (SDN) ecosystem?

* [ ] Physical router manufacturing platform
* [ ] Network traffic visualization tool
* [ ] Open-source SDN controller framework
* [ ] Switch firmware management system

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Open-source SDN controller framework
💡 OpenDaylight acts as a centralized SDN controller providing control-plane logic, APIs, and protocol plugins for programmable networks.

</details>

---

### 82. In OpenDaylight architecture, what is the primary responsibility of the Model-Driven Service Abstraction Layer (MD-SAL)?

* [ ] Monitoring switch performance metrics
* [ ] Abstracting network services using YANG-based data models
* [ ] Encrypting southbound traffic
* [ ] Managing physical device firmware

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Abstracting network services using YANG-based data models
💡 MD-SAL provides a model-driven framework where applications interact through YANG-defined data and services.

</details>

---

### 83. Which OpenDaylight component enables OpenFlow-based southbound communication with switches?

* [ ] RESTCONF
* [ ] NETCONF
* [ ] OpenFlow Plugin
* [ ] BGP-LS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OpenFlow Plugin
💡 The OpenFlow plugin allows the controller to install, modify, and delete flow entries in OpenFlow-enabled switches.

</details>

---

### 84. OpenDaylight relies heavily on which programming concept to support modularity and dynamic service loading?

* [ ] Functional programming
* [ ] Reactive streams
* [ ] OSGi framework
* [ ] Container orchestration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OSGi framework
💡 OSGi enables OpenDaylight to deploy modular bundles dynamically, improving extensibility and maintainability.

</details>

---

### 85. What is the most significant advantage of separating the control plane from the data plane in SDN?

* [ ] Increased packet encryption
* [ ] Reduced IP address usage
* [ ] Centralized programmability and policy enforcement
* [ ] Lower hardware power consumption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centralized programmability and policy enforcement
💡 Control-plane separation enables centralized intelligence, dynamic policy enforcement, and automation.

</details>

---

### 86. Which real-world use case best demonstrates the benefits of SDN and OpenFlow?

* [ ] Static routing in small LANs
* [ ] Dynamic traffic engineering and load balancing
* [ ] Client-side caching
* [ ] DNS resolution

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamic traffic engineering and load balancing
💡 SDN enables real-time traffic optimization based on network conditions.

</details>

---

### 87. What is the primary purpose of RESTCONF in OpenDaylight?

* [ ] Encrypt controller communications
* [ ] Provide RESTful access to YANG-modeled data and services
* [ ] Automatically upgrade switch firmware
* [ ] Perform DNS zone transfers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provide RESTful access to YANG-modeled data and services
💡 RESTCONF allows northbound applications to interact with the controller using standard REST APIs.

</details>

---

### 88. Which internal OpenDaylight component stores both intended configurations and real-time operational state?

* [ ] Flow tables
* [ ] VLAN database
* [ ] MD-SAL datastore
* [ ] ARP cache

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MD-SAL datastore
💡 The datastore maintains **config** (intended state) and **operational** (actual state) data.

</details>

---

### 89. In production OpenFlow deployments, which challenge is most commonly encountered?

* [ ] HTTP incompatibility
* [ ] IP address exhaustion
* [ ] Interoperability with legacy network devices
* [ ] High packet loss on wired links

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Interoperability with legacy network devices
💡 Integrating SDN with traditional networks remains a key deployment challenge.

</details>

---

### 90. What is Mininet primarily used for in SDN development?

* [ ] Managing physical switches
* [ ] Simulating virtual network topologies for testing controllers
* [ ] Encrypting control traffic
* [ ] Monitoring hardware failures

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Simulating virtual network topologies for testing controllers
💡 Mininet provides lightweight network emulation using software switches and hosts.

</details>

---

### 91. How does the L2Switch application in OpenDaylight populate its forwarding table?

* [ ] Static administrator configuration
* [ ] DHCP snooping
* [ ] Learning source MAC addresses from incoming frames
* [ ] Querying an external directory service

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Learning source MAC addresses from incoming frames
💡 The L2Switch application behaves like a learning Ethernet switch.

</details>

---

### 92. Which clustering approach is supported by OpenDaylight to achieve high availability?

* [ ] Active-passive without state sharing
* [ ] Hardware-based clustering
* [ ] Active-active clustering with distributed state
* [ ] Single-node redundancy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active-active clustering with distributed state
💡 Multiple controller instances share state using a distributed datastore.

</details>

---

### 93. In MD-SAL, how are network events typically delivered to applications?

* [ ] SNMP traps
* [ ] Hardware interrupts
* [ ] Publish-subscribe notifications via datastore changes
* [ ] REST polling only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Publish-subscribe notifications via datastore changes
💡 Applications subscribe to datastore updates and receive event notifications.

</details>

---

### 94. What ensures consistency of replicated data across OpenDaylight cluster nodes?

* [ ] TLS encryption
* [ ] Raft consensus algorithm
* [ ] RESTCONF transactions
* [ ] OpenFlow barriers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Raft consensus algorithm
💡 Raft ensures leader election, log replication, and strong consistency.

</details>

---

### 95. Which MD-SAL datastore holds the *intended* configuration of the network?

* [ ] Operational datastore
* [ ] Config datastore
* [ ] Backup datastore
* [ ] Cache datastore

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Config datastore
💡 The config datastore represents the desired network state.

</details>

---

### 96. How does Open vSwitch implement tunneling protocols like VXLAN?

* [ ] Dedicated hardware accelerators
* [ ] Software-based virtual ports in the kernel or userspace
* [ ] External gateway appliances
* [ ] It does not support tunneling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Software-based virtual ports in the kernel or userspace
💡 OVS supports multiple tunneling protocols through software abstraction.

</details>

---

### 97. How does the L2Switch application handle Ethernet broadcast frames?

* [ ] Drops all broadcasts
* [ ] Floods frames to all ports except the source
* [ ] Converts broadcasts to multicast
* [ ] Routes them via Layer-3 logic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Floods frames to all ports except the source
💡 This behavior mimics traditional Ethernet switching.

</details>

---

### 98. What internal consistency model does MD-SAL primarily rely on?

* [ ] Eventual consistency without locking
* [ ] Strong consistency using transactional updates
* [ ] Read-only replication
* [ ] No defined consistency guarantees

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Strong consistency using transactional updates
💡 MD-SAL uses optimistic locking and transactions for data integrity.

</details>

---

### 99. How does OpenDaylight support multiple southbound protocols?

* [ ] Single monolithic design
* [ ] Modular plugin-based architecture
* [ ] REST-only communication
* [ ] Proprietary closed-source protocols

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Modular plugin-based architecture
💡 OpenDaylight supports OpenFlow, NETCONF, BGP, OVSDB, and more via plugins.

</details>

---

### 100. In OpenDaylight, AAA refers to which security framework?

* [ ] Application Abstraction Architecture
* [ ] Authentication, Authorization, and Accounting
* [ ] Access Allocation Automation
* [ ] Association and Analysis Architecture

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication, Authorization, and Accounting
💡 AAA enforces identity verification, access control, and activity logging.

</details>

---

### 101. Which OpenDaylight service manages user roles and permissions?

* [ ] MD-SAL
* [ ] OpenFlow Plugin
* [ ] AAA Service
* [ ] LISP Plugin

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AAA Service
💡 The AAA service integrates authentication backends and role-based access control.

</details>

---

### 102. What is the primary function of OVSDB in OpenDaylight?

* [ ] Encrypting control traffic
* [ ] Managing virtual switch configuration and state
* [ ] Monitoring controller logs
* [ ] Storing YANG models

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Managing virtual switch configuration and state
💡 OVSDB provides programmatic control over Open vSwitch instances.

</details>

---

### 103. Group Based Policy (GBP) is mainly used to achieve which SDN objective?

* [ ] IP address management
* [ ] User authentication
* [ ] Intent-based policy definition and enforcement
* [ ] Flow rule compression

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Intent-based policy definition and enforcement
💡 GBP abstracts policies from low-level network configurations.

</details>

---

### 104. Which OpenDaylight component enables service chaining of firewalls, IDS, and DPI?

* [ ] Virtual Tenant Network
* [ ] Service Function Chaining (SFC)
* [ ] OpenFlow Plugin
* [ ] BGP Plugin

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Service Function Chaining (SFC)
💡 SFC defines ordered traversal of network services.

</details>

---

### 105. LISP Flow Mapping in OpenDaylight is associated with which networking concept?

* [ ] MAC address filtering
* [ ] Endpoint identifier and locator separation
* [ ] VLAN segmentation
* [ ] DNS resolution

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Endpoint identifier and locator separation
💡 LISP decouples identity (EID) from location (RLOC).

</details>

---

### 106. In OpenDaylight, what defines permitted communication between endpoint groups in GBP?

* [ ] MAC access lists
* [ ] Contracts
* [ ] Flow tables
* [ ] IP blocks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Contracts
💡 Contracts specify allowed interactions between endpoint groups.

</details>

---

### 107. Which backend systems are commonly integrated with OpenDaylight AAA?

* [ ] Flat files only
* [ ] LDAP or RADIUS servers
* [ ] SNMP managers
* [ ] Proprietary scripts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** LDAP or RADIUS servers
💡 AAA integrates with enterprise authentication systems.

</details>

---

### 108. In OpenDaylight’s LISP implementation, where are EID-to-RLOC mappings maintained?

* [ ] ARP cache
* [ ] Global Mapping System (Map Server/Resolver)
* [ ] DNS servers
* [ ] Flow cache

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Global Mapping System (Map Server/Resolver)
💡 The mapping system resolves endpoint identities to routing locators.

</details>

---
