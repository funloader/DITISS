> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---
# 230 MCQ Set

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

### 109. Which command is used to view the dynamic IP-to-MAC address mappings learned by a host on a local network?

* [ ] netstat
* [ ] ipconfig
* [ ] arp
* [ ] ping

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** arp
💡 The `arp` command displays the ARP cache containing IP-MAC address mappings learned via ARP.

</details>

---

### 110. Which core function is performed by the Data Link layer in Ethernet networks?

* [ ] Error correction
* [ ] Route identification
* [ ] Encryption
* [ ] Error detection

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Error detection
💡 Ethernet uses Frame Check Sequence (FCS) at Layer 2 for error detection, not correction.

</details>

---

### 111. When a host initiates a ping request, which ICMP message type is sent first?

* [ ] Echo Reply
* [ ] Ping request
* [ ] Echo Request
* [ ] Ping reply

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Echo Request
💡 ICMP Echo Request is sent by the source; Echo Reply is returned by the destination.

</details>

---

### 112. What is the first field in an Ethernet frame (excluding the preamble)?

* [ ] Source MAC address
* [ ] EtherType
* [ ] Payload data
* [ ] Destination MAC address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Destination MAC address
💡 Ethernet frames always begin with the destination MAC to allow proper frame delivery.

</details>

---

### 113. What is the maximum standard Ethernet frame size (without jumbo frames)?

* [ ] 64 bytes
* [ ] 600 bytes
* [ ] 1518 bytes
* [ ] 1024 bytes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1518 bytes
💡 This includes header and FCS but excludes the preamble.

</details>

---

### 114. Which protocol prevents switching loops in managed Ethernet switches?

* [ ] ICMP
* [ ] VTP
* [ ] NNTP
* [ ] STP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** STP
💡 Spanning Tree Protocol (STP) prevents Layer-2 broadcast storms caused by loops.

</details>

---

### 115. How much data is typically stored in a single hard disk sector?

* [ ] 512 bytes
* [ ] 512 KB
* [ ] 512 MB
* [ ] 512 GB

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 512 bytes
💡 Traditional disk sectors store 512 bytes (modern disks may support 4K sectors).

</details>

---

### 116. Fixed partition memory management primarily suffers from which type of fragmentation?

* [ ] External
* [ ] Complete
* [ ] Internal
* [ ] Partial

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Internal
💡 Fixed partitions cause wasted memory inside allocated partitions.

</details>

---

### 117. Which IP flag is used in Path MTU Discovery to determine the maximum supported MTU?

* [ ] SYN
* [ ] RST
* [ ] ACK
* [ ] Don’t Fragment

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Don’t Fragment
💡 The DF flag ensures routers return ICMP errors instead of fragmenting packets.

</details>

---

### 118. Which Cisco IOS prompt mode allows execution of the command `copy running-config startup-config`?

* [ ] Switch-6J>
* [ ] Switch-6J(config)#
* [ ] Switch-6J#
* [ ] Switch-6J(config-if)#

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Switch-6J#
💡 Privileged EXEC mode is required for configuration copy operations.

</details>

---

### 119. Which application is commonly used for terminal emulation over a router’s console port?

* [ ] HyperTerminal
* [ ] Secure Shell
* [ ] Internet Explorer
* [ ] Telnet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HyperTerminal
💡 Terminal emulators provide serial console access for initial router configuration.

</details>

---

### 120. Which Cisco IOS command displays RIP routing updates in real time?

* [ ] show ip route
* [ ] debug ip rip
* [ ] show protocols
* [ ] debug ip route

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** debug ip rip
💡 This command shows RIP advertisements being sent and received.

</details>

---

### 121. Which feature exists in IPv6 but not in IPv4?

* [ ] Fragmentation
* [ ] Header checksum
* [ ] Options
* [ ] Anycast addressing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Anycast addressing
💡 IPv6 natively supports Anycast; IPv4 does not define it explicitly.

</details>

---

### 122. ICMP was primarily designed to provide which functionality?

* [ ] Error reporting
* [ ] Error correction
* [ ] Host management queries
* [ ] All of the mentioned

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the mentioned
💡 ICMP supports error reporting and network diagnostic messages.

</details>

---

### 123. Which authentication protocol avoids sending the actual password over the network?

* [ ] LAPB
* [ ] PAP
* [ ] Frame Relay
* [ ] CHAP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CHAP
💡 CHAP uses challenge-response hashing for secure authentication.

</details>

---

### 124. Which Wi-Fi security mode integrates a RADIUS server for enterprise-level authentication?

* [ ] WEP
* [ ] WPA-Enterprise
* [ ] WPA-Personal
* [ ] TKIP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** WPA-Enterprise
💡 WPA-Enterprise uses 802.1X and RADIUS for centralized authentication.

</details>

---

### 125. Which ICMP type is generated when a packet’s TTL value reaches zero?

* [ ] 0
* [ ] 3
* [ ] 8
* [ ] 11

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 11
💡 ICMP Type 11 indicates “Time Exceeded.”

</details>

---

### 126. For which application is UDP generally unsuitable?

* [ ] DNS
* [ ] SNMP
* [ ] RTP
* [ ] SMTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SMTP
💡 SMTP requires reliable, connection-oriented communication provided by TCP.

</details>

---

### 127. Which cable type is best suited for long-distance, high-bandwidth communication?

* [ ] UTP
* [ ] Multimode fiber
* [ ] STP
* [ ] Single-mode fiber

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Single-mode fiber
💡 Single-mode fiber supports long distances with minimal signal loss.

</details>

---

### 128. A packet delivered to all hosts within a network using a special destination address is called:

* [ ] Multicasting
* [ ] Broadcasting
* [ ] Unicasting
* [ ] Anycasting

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Broadcasting
💡 Broadcast frames are processed by all nodes in the broadcast domain.

</details>

---

### 129. Which OS command displays the routing table of a host machine?

* [ ] arp -all
* [ ] netstat -r
* [ ] showroute -all
* [ ] Only routers have routing tables

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** netstat -r
💡 End systems maintain routing tables for packet forwarding decisions.

</details>

---

### 130. An inbound ACL blocks TCP/UDP ports 21, 23, and 25. Which traffic will still be allowed?

* [ ] HTTP
* [ ] SMTP
* [ ] TELNET
* [ ] FTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HTTP
💡 HTTP uses TCP port 80, which is not blocked.

</details>

---

### 131. What type of network architecture exists when no node has a dedicated server role?

* [ ] Mainframe
* [ ] Peer-to-peer
* [ ] Client-server
* [ ] Centralized

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Peer-to-peer
💡 All nodes act as both clients and servers.

</details>

---

### 132. Which router configuration mode is required to configure SSH or Telnet access?

* [ ] Line configuration mode
* [ ] Global configuration mode
* [ ] Router configuration mode
* [ ] Interface configuration mode

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Line configuration mode
💡 Remote access parameters are configured under VTY lines.

</details>

---

### 133. In packet-switched networks, what ensures correct packet reassembly?

* [ ] Source address
* [ ] Sequence number
* [ ] Priority value
* [ ] Destination address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Sequence number
💡 Sequence numbers allow proper ordering at the destination.

</details>

---

### 134. A cable wired T568A on one end and T568B on the other is known as:

* [ ] Patch cable
* [ ] Console cable
* [ ] Crossover cable
* [ ] Straight-through cable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Crossover cable
💡 Crossover cables swap transmit and receive pairs.

</details>

---

### 135. Which statement about Layer-3 addresses is correct?

* [ ] They are physical addresses
* [ ] They are used in routing decisions
* [ ] They are used only locally
* [ ] They change at every router

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They are used in routing decisions
💡 IP addresses guide routers in forwarding packets.

</details>

---

### 136. Which port is commonly used to connect a router’s console cable?

* [ ] RS-232 serial
* [ ] Parallel
* [ ] IEEE-1394
* [ ] PS/2

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RS-232 serial
💡 Console access uses serial communication.

</details>

---

### 137. What is the state of a process that is ready to execute but swapped out of memory?

* [ ] Ready Suspended
* [ ] Blocked
* [ ] Ready
* [ ] Blocked Suspended

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ready Suspended
💡 The process is ready but resides in secondary storage.

</details>

---

### 138. Which IPv4 header field is NOT related to fragmentation?

* [ ] Identification
* [ ] Fragment Offset
* [ ] Type of Service
* [ ] Flags

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Type of Service
💡 ToS is used for QoS, not fragmentation.

</details>

---

### 139. Which buffer speeds up logical-to-physical address translation in paging?

* [ ] Translation Lookaside Buffer
* [ ] Input buffer
* [ ] Segment buffer
* [ ] Translation local buffer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Translation Lookaside Buffer
💡 TLB caches recent page table entries.

</details>

---

### 140. Which TCP flag does NOT cause a state transition?

* [ ] PSH
* [ ] RST
* [ ] SYN
* [ ] FIN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PSH
💡 PSH only controls buffering behavior.

</details>

---

### 141. OSPF and BGP are classified as:

* [ ] Inter-AS & Intra-AS routing respectively
* [ ] Intra-AS & Inter-AS routing respectively
* [ ] Both Intra-AS
* [ ] Both Inter-AS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Intra-AS & Inter-AS routing respectively
💡 OSPF is an IGP; BGP is an EGP.

</details>

---

### 142. What mechanism resolves a domain name to its corresponding IP address?

* [ ] Forward Lookup Zone
* [ ] Forwarder
* [ ] Reverse Lookup Zone
* [ ] DHCP scope

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forward Lookup Zone
💡 Forward lookup resolves FQDN → IP.

</details>

---

### 143. Which server centralizes authentication for Cisco network devices?

* [ ] Active Directory
* [ ] AAA server
* [ ] 802.1X server
* [ ] Terminal server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AAA server
💡 AAA servers manage authentication, authorization, and accounting.

</details>

---

### 144. Which routing approach adapts automatically to changing network conditions?

* [ ] Static routing
* [ ] Fixed alternative routing
* [ ] Standard routing
* [ ] Dynamic routing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamic routing
💡 Dynamic protocols adjust routes based on topology changes.

</details>

---

### 145. What is the destination MAC address of an ARP request frame?

* [ ] Broadcast IP
* [ ] Broadcast MAC
* [ ] Default gateway IP
* [ ] Default gateway MAC

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Broadcast MAC
💡 ARP requests are sent to FF:FF:FF:FF:FF:FF.

</details>

---

### 146. Why are twisted pairs used in UTP cables?

* [ ] To reduce cost
* [ ] To reduce cable thickness
* [ ] To reduce electromagnetic interference
* [ ] To increase bandwidth artificially

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To reduce electromagnetic interference
💡 Twisting minimizes crosstalk and noise.

</details>

---

### 147. What is the decimal equivalent of binary number 11011010?

* [ ] 186
* [ ] 222
* [ ] 202
* [ ] 218

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 218
💡 128+64+16+8+2 = 218.

</details>

---

### 148. What enables applications to communicate using standard OS-supported networking mechanisms?

* [ ] Sockets
* [ ] Protocols
* [ ] Ethernet
* [ ] OSI layers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Sockets
💡 Sockets provide the programming interface for network communication.

</details>

---

### 149. During a CAM table overflow attack on a Layer-2 switch, how does the switch handle incoming frames whose destination MAC addresses are unknown?

* [ ] Switch drops all unknown unicast frames
* [ ] Switch forwards frames only to the default gateway
* [ ] Switch sends frames to the CPU for processing
* [ ] Switch floods frames out of all ports except the source port

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Switch floods frames out of all ports except the source port
💡 When the CAM table is full, the switch behaves like a hub for unknown unicasts, leading to flooding and potential sniffing attacks.

</details>

---

### 150. Which protocol does **not** provide reliable, connection-oriented data delivery?

* [ ] TCP
* [ ] UDP
* [ ] FTP
* [ ] Telnet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** UDP
💡 UDP is connectionless and does not guarantee delivery, ordering, or retransmission.

</details>

---

### 151. An IPv4 address **172.16.48.129/20** belongs to which subnet range?

* [ ] 172.16.0.0 – 172.16.15.255
* [ ] 172.16.32.0 – 172.16.47.255
* [ ] 172.16.48.0 – 172.16.63.255
* [ ] 172.16.48.0 – 172.16.49.255

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 172.16.48.0 – 172.16.63.255
💡 A /20 subnet increments by 16 in the third octet (48–63).

</details>

---

### 152. In an OSPF broadcast network, what is the primary responsibility of the Designated Router (DR)?

* [ ] Assign IP addresses to routers
* [ ] Manage multicast group membership
* [ ] Reduce LSA flooding by acting as a central exchange
* [ ] Perform Network Address Translation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduce LSA flooding by acting as a central exchange
💡 DR minimizes adjacencies and LSA flooding in multi-access networks.

</details>

---

### 153. Which parameter is evaluated **first** during OSPF DR election on a broadcast network?

* [ ] Highest Router ID
* [ ] Lowest MAC address
* [ ] Highest OSPF priority
* [ ] Interface bandwidth

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Highest OSPF priority
💡 Router priority is evaluated first; Router ID is used only as a tiebreaker.

</details>

---

### 154. Which routing protocol uses **UDP port 520** and a **hop-count metric**?

* [ ] OSPF
* [ ] RIP
* [ ] IGRP
* [ ] EIGRP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RIP
💡 RIP uses hop count as its metric with a maximum of 15 hops.

</details>

---

### 155. What is the **administrative distance** of **EIGRP internal routes**?

* [ ] 110
* [ ] 90
* [ ] 120
* [ ] 100

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 90
💡 EIGRP internal routes are highly preferred due to low AD.

</details>

---

### 156. When multiple ACL entries match a packet, which ACL rule is applied by a Cisco router?

* [ ] Last matching entry
* [ ] Most specific entry
* [ ] Random entry
* [ ] First matching entry from top to bottom

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** First matching entry from top to bottom
💡 ACLs are processed sequentially; first match wins.

</details>

---

### 157. How does Spanning Tree Protocol (STP) prevent Layer-2 switching loops?

* [ ] By load balancing traffic
* [ ] By dynamically routing packets
* [ ] By placing redundant ports into a blocking state
* [ ] By disabling broadcast frames

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** By placing redundant ports into a blocking state
💡 STP logically blocks redundant paths while maintaining physical redundancy.

</details>

---

### 158. Given network **192.168.1.64/27**, what is the valid host IP range?

* [ ] 192.168.1.64 – 192.168.1.95
* [ ] 192.168.1.65 – 192.168.1.94
* [ ] 192.168.1.66 – 192.168.1.93
* [ ] 192.168.1.64 – 192.168.1.94

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 192.168.1.65 – 192.168.1.94
💡 Network = .64, Broadcast = .95, usable hosts in between.

</details>

---

### 159. A switch receives a frame destined for an unknown MAC address. What action does it take?

* [ ] Drops the frame
* [ ] Floods the frame to all ports except the source
* [ ] Sends it to the default gateway
* [ ] Logs an error and discards the frame

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Floods the frame to all ports except the source
💡 This is known as unknown unicast flooding.

</details>

---

### 160. Which field enables VLAN separation on a trunk link?

* [ ] Source MAC address
* [ ] Destination MAC address
* [ ] IEEE 802.1Q VLAN tag
* [ ] Frame Check Sequence

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IEEE 802.1Q VLAN tag
💡 VLAN ID inside the 802.1Q tag identifies VLAN membership.

</details>

---

### 161. Which scenario does **not** justify the use of VLSM?

* [ ] Conserving IP address space
* [ ] Designing subnets of varying sizes
* [ ] Implementing classless routing
* [ ] Subnetting networks requiring identical host counts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Subnetting networks requiring identical host counts
💡 Fixed-size subnetting does not require VLSM.

</details>

---

### 162. What critical information does the `show version` command provide on a Cisco router?

* [ ] MAC address table
* [ ] Startup configuration
* [ ] IOS version and configuration register
* [ ] Routing protocol statistics

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IOS version and configuration register
💡 Useful for troubleshooting boot and IOS issues.

</details>

---

### 163. Match the correct Protocol Data Units (PDUs) for OSI Layers 3, 4, and 2 respectively.

* [ ] Frame, Segment, Packet
* [ ] Packet, Segment, Frame
* [ ] Segment, Packet, Frame
* [ ] Datagram, Frame, Segment

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Packet, Segment, Frame
💡 Layer 3 = Packet, Layer 4 = Segment, Layer 2 = Frame.

</details>

---

### 164. Which command assigns an IP address to a router sub-interface in a Router-on-a-Stick configuration?

* [ ] ip vlan
* [ ] switchport mode access
* [ ] ip address
* [ ] encapsulation dot1q

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ip address
💡 IP is assigned after defining the VLAN encapsulation.

</details>

---

### 165. What is the primary function of NCP in PPP?

* [ ] Authentication
* [ ] Link establishment
* [ ] Error detection
* [ ] Network-layer protocol configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network-layer protocol configuration
💡 NCP configures IP, IPv6, and other Layer-3 protocols.

</details>

---

### 166. How many **usable host IPs** are available in a **/25 subnet**?

* [ ] 64
* [ ] 126
* [ ] 128
* [ ] 254

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 126
💡 /25 provides 128 total addresses minus network and broadcast.

</details>

---

### 167. Which of the following is a **valid IPv6 multicast address**?

* [ ] 2001::1
* [ ] FF02::1
* [ ] FE80::1
* [ ] ::1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** FF02::1
💡 IPv6 multicast addresses always start with FF.

</details>

---

### 168. What metric components does EIGRP use to compute the best path?

* [ ] Hop count only
* [ ] Bandwidth and delay
* [ ] Bandwidth only
* [ ] Cost

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bandwidth and delay
💡 These are primary components of the EIGRP composite metric.

</details>

---

### 169. You need three VLANs for **90, 50, and 20 users**. Which VLSM allocation is optimal?

* [ ] /25, /26, /27
* [ ] /24, /24, /24
* [ ] /26, /27, /28
* [ ] /23, /24, /26

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /25, /26, /27
💡 Each subnet efficiently matches host requirements.

</details>

---

### 170. Which transport-layer mechanism prevents a fast sender from overwhelming a slow receiver?

* [ ] MAC filtering
* [ ] IP fragmentation
* [ ] Flow control
* [ ] Segmentation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Flow control
💡 TCP flow control uses window size to regulate data flow.

</details>

---

### 171. Two routers are connected via a serial interface. What is the default encapsulation?

* [ ] PPP
* [ ] SLIP
* [ ] HDLC
* [ ] Ethernet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HDLC
💡 Cisco routers use HDLC by default on serial links.

</details>

---

### 172. What is the function of the **Magic Number** field in PPP?

* [ ] Authenticate the peer
* [ ] Validate frame size
* [ ] Detect looped links
* [ ] Negotiate encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Detect looped links
💡 Magic numbers help detect misconfigurations causing loops.

</details>

---

### 173. Which Cisco IOS mode allows only basic monitoring commands?

* [ ] Privileged EXEC
* [ ] ROMMON
* [ ] User EXEC
* [ ] Global Configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** User EXEC
💡 User EXEC has limited, non-destructive commands.

</details>

---

### 174. What is the primary purpose of STP BPDUs?

* [ ] Prevent broadcast storms
* [ ] Elect the root bridge and maintain topology
* [ ] Assign IP addresses
* [ ] Configure VLANs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Elect the root bridge and maintain topology
💡 BPDUs carry STP information between switches.

</details>

---

### 175. Which routing protocol **does not use multicast** for updates?

* [ ] OSPF
* [ ] RIP v2
* [ ] EIGRP
* [ ] RIP v1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RIP v1
💡 RIP v1 uses broadcast instead of multicast.

</details>

---

### 176. ACLs that filter traffic based on **IP address, protocol, and port number** are:

* [ ] Standard ACLs
* [ ] Dynamic ACLs
* [ ] Extended ACLs
* [ ] Reflexive ACLs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Extended ACLs
💡 Extended ACLs provide granular traffic control.

</details>

---

### 177. A router is connected to a switch via a trunk link to route VLAN traffic. What configuration is required?

* [ ] Static routing
* [ ] RIP
* [ ] Router-on-a-Stick
* [ ] Access port configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Router-on-a-Stick
💡 Sub-interfaces handle inter-VLAN routing.

</details>

---

### 178. What is the main function of the **Presentation Layer** in the OSI model?

* [ ] Session management
* [ ] Encryption and compression
* [ ] Port addressing
* [ ] Path determination

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encryption and compression
💡 It ensures data is in a usable format for the application.

</details>

---

### 179. By default, a Class C network supports how many usable hosts?

* [ ] 254
* [ ] 126
* [ ] 64
* [ ] 510

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 254
💡 256 total minus network and broadcast.

</details>

---

### 180. What is the IPv6 loopback address?

* [ ] ::
* [ ] ::1
* [ ] FF00::1
* [ ] FE80::1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ::1
💡 Equivalent to IPv4 127.0.0.1.

</details>

---

### 181. What traffic is permitted by the ACL entry:

`access-list 101 permit tcp any host 10.10.10.1 eq 80`?

* [ ] HTTPS traffic
* [ ] ICMP traffic
* [ ] HTTP traffic
* [ ] Telnet traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HTTP traffic
💡 Port 80 corresponds to HTTP.

</details>

---

### 182. If no ACL is applied on a Cisco router interface, what happens to traffic?

* [ ] All traffic denied
* [ ] All traffic permitted
* [ ] Only ICMP allowed
* [ ] Only TCP forwarded

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All traffic permitted
💡 ACLs are implicit deny only when applied.

</details>

---

### 183. Which cable is used for **100Base-TX Ethernet**?

* [ ] Coaxial
* [ ] Fiber optic
* [ ] Twisted-pair Cat5e
* [ ] Shielded twisted pair (STP)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Twisted-pair Cat5e
💡 100Base-TX requires Cat5 or better.

</details>

---

### 184. What is the broadcast address for **192.168.3.0/26**?

* [ ] 192.168.3.127
* [ ] 192.168.3.63
* [ ] 192.168.3.255
* [ ] 192.168.3.191

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 192.168.3.63
💡 /26 blocks increment by 64.

</details>

---

### 185. Which Ethernet frame field supports VLAN identification?

* [ ] EtherType
* [ ] FCS
* [ ] 802.1Q VLAN tag
* [ ] IP protocol field

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 802.1Q VLAN tag
💡 Contains VLAN ID and priority bits.

</details>

---

### 186. In STP, if two switches have identical bridge priority values, how is the root bridge chosen?

* [ ] Random selection
* [ ] Highest bandwidth
* [ ] Lowest MAC address
* [ ] First booted switch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lowest MAC address
💡 MAC address acts as the final tie-breaker.

</details>

---

### 187. Which subnet mask provides **6 usable host IP addresses**?

* [ ] 255.255.255.248
* [ ] 255.255.255.240
* [ ] 255.255.255.252
* [ ] 255.255.255.255

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 255.255.255.248
💡 /29 → 8 total, 6 usable.

</details>

---

### 188. In a PPP-based WAN link, which authentication protocol is considered **more secure**?

* [ ] PAP
* [ ] RADIUS
* [ ] CHAP
* [ ] Telnet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CHAP
💡 CHAP uses challenge-response and avoids plaintext passwords.

</details>

---

### 189. Which statement best explains the significance of Classless Inter-Domain Routing (CIDR) in modern IP networking?

* [ ] CIDR is applicable only to IPv6 networks and eliminates subnet masks
* [ ] CIDR restricts address aggregation to fixed class boundaries
* [ ] CIDR replaces classful addressing and enables flexible prefix lengths for efficient IP utilization
* [ ] CIDR mandates the use of static routing to function correctly

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CIDR replaces classful addressing and enables flexible prefix lengths for efficient IP utilization
💡 CIDR allows variable-length subnet masks (VLSM), removing class boundaries and enabling route aggregation, which significantly conserves IPv4 address space.

</details>

---

### 190. You are designing an IP addressing scheme that must support **at least 5 subnets**, each requiring **a minimum of 30 usable host addresses**. Which subnet mask best satisfies this requirement?

* [ ] 255.255.255.224 (/27)
* [ ] 255.255.255.240 (/28)
* [ ] 255.255.255.248 (/29)
* [ ] 255.255.255.192 (/26)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 255.255.255.224 (/27)
💡 A /27 subnet provides 32 total addresses and 30 usable hosts, making it the smallest mask that satisfies the requirement efficiently.

</details>

---

### 191. A Layer-2 switch receives a broadcast Ethernet frame on one of its ports. How does the switch handle this frame?

* [ ] Forwards the frame only to ports in the same VLAN
* [ ] Drops the broadcast frame by default
* [ ] Forwards the frame out all ports except the incoming port
* [ ] Sends the frame to the router for further processing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forwards the frame out all ports except the incoming port
💡 Broadcast frames are flooded by switches within the same VLAN to ensure all devices receive them.

</details>

---

### 192. What is the primary purpose of implementing Access Control Lists (ACLs) on routers or switches?

* [ ] To dynamically assign IP addresses
* [ ] To encrypt traffic between communicating hosts
* [ ] To filter and control network traffic based on defined rules
* [ ] To detect and correct physical layer transmission errors

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To filter and control network traffic based on defined rules
💡 ACLs are rule-based filters that permit or deny packets based on parameters such as IP address, protocol, and port number.

</details>

---

### 193. Which combination of protocols works together to automatically assign IP addresses to hosts and resolve hostnames to IP addresses?

* [ ] TCP and IP
* [ ] DNS and DHCP
* [ ] FTP and HTTP
* [ ] NAT and RADIUS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS and DHCP
💡 DHCP provides IP configuration, while DNS resolves domain names to IP addresses, enabling seamless network communication.

</details>

---

### 194. Which statement best describes how Point-to-Point Protocol (PPP) improves communication over traditional serial link protocols?

* [ ] It provides encryption for all Layer-3 traffic by default
* [ ] It supports multiple Layer-3 protocols and offers authentication mechanisms
* [ ] It enables wireless connectivity using MAC-layer framing
* [ ] It performs VLAN tagging across serial interfaces

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It supports multiple Layer-3 protocols and offers authentication mechanisms
💡 PPP encapsulates various network layer protocols and supports authentication methods like PAP and CHAP, unlike older protocols such as HDLC.

</details>

---

### 195. A router receives a packet destined for a network that does not exist in its routing table. What action will the router take if a default route is configured?

* [ ] Drop the packet immediately
* [ ] Send an ICMP redirect to the source
* [ ] Forward the packet using the default route
* [ ] Broadcast the packet on all interfaces

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forward the packet using the default route
💡 A default route (0.0.0.0/0) acts as a gateway of last resort for unknown destinations.

</details>

---

### 196. In the OSI reference model, which layer is responsible for session establishment, maintenance, synchronization, and termination between applications?

* [ ] Presentation
* [ ] Session
* [ ] Transport
* [ ] Application

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Session
💡 The Session layer manages dialog control, checkpoints, and session recovery between communicating applications.

</details>

---

### 197. Which statement about Virtual Local Area Networks (VLANs) is technically accurate?

* [ ] VLANs operate exclusively at the Physical layer
* [ ] VLANs require a Layer-3 switch to exist
* [ ] VLANs logically segment broadcast domains within a switch
* [ ] VLANs completely block communication between all switch ports

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLANs logically segment broadcast domains within a switch
💡 VLANs allow logical segmentation independent of physical topology, improving security and reducing broadcast traffic.

</details>

---

### 198. Which protocol is used to resolve an IPv4 address to its corresponding MAC address within a local network?

* [ ] DNS
* [ ] ICMP
* [ ] ARP
* [ ] DHCP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ARP
💡 Address Resolution Protocol (ARP) maps IP addresses to MAC addresses for local network communication.

</details>

---

### 199. Which routing protocol uses a composite metric based on bandwidth and delay and supports unequal-cost load balancing?

* [ ] RIP
* [ ] IGRP
* [ ] EIGRP
* [ ] OSPF

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EIGRP
💡 EIGRP uses a composite metric and supports unequal-cost load balancing via the variance feature.

</details>

---

### 200. While configuring NAT, which technique allows multiple private IP addresses to share a single public IP using different port numbers?

* [ ] Static NAT
* [ ] Dynamic NAT
* [ ] Port Address Translation (PAT)
* [ ] One-to-One NAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Port Address Translation (PAT)
💡 PAT, also known as NAT overload, differentiates sessions using TCP/UDP port numbers.

</details>

---

### 201. Which IPv6 address range is reserved specifically for link-local communication?

* [ ] FE80::/10
* [ ] FC00::/7
* [ ] 2000::/3
* [ ] FFFF::/16

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** FE80::/10
💡 Link-local IPv6 addresses are automatically assigned and used for communication within the local segment.

</details>

---

### 202. Which Cisco IOS command is used to display the current IPv4 routing table?

* [ ] show interface status
* [ ] show running-config
* [ ] show ip route
* [ ] show version

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** show ip route
💡 This command displays all learned routes, routing protocols, metrics, and next-hop information.

</details>

---

### 203. How does Spanning Tree Protocol (STP) prevent switching loops in a Layer-2 network?

* [ ] Disables MAC learning on non-root switches
* [ ] Blocks redundant paths to maintain a loop-free topology
* [ ] Divides the network into multiple broadcast domains
* [ ] Forwards frames only to manually configured ports

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Blocks redundant paths to maintain a loop-free topology
💡 STP calculates the best path to the root bridge and blocks alternate paths to prevent loops.

</details>

---

### 204. What is the maximum number of usable host addresses available in a /26 IPv4 subnet?

* [ ] 62
* [ ] 64
* [ ] 30
* [ ] 126

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 62
💡 A /26 subnet provides 64 total addresses; subtracting network and broadcast leaves 62 usable hosts.

</details>

---

### 205. What is the primary role of TACACS+ in enterprise network security?

* [ ] Encrypts all end-user data traffic
* [ ] Provides NAT functionality
* [ ] Separates authentication, authorization, and accounting processes
* [ ] Resolves domain names

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Separates authentication, authorization, and accounting processes
💡 TACACS+ provides granular AAA control and encrypts the entire payload, unlike RADIUS.

</details>

---

### 206. Which statement correctly describes RADIUS?

* [ ] Encrypts the entire packet payload
* [ ] Used for routing decisions between routers
* [ ] Combines authentication and authorization
* [ ] Functions only on Cisco devices

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Combines authentication and authorization
💡 RADIUS integrates authentication and authorization and encrypts only the password field.

</details>

---

### 207. What is the primary advantage of implementing Variable Length Subnet Masking (VLSM)?

* [ ] Simplifies routing configuration
* [ ] Creates equal-sized subnets
* [ ] Improves IP address utilization
* [ ] Eliminates routing loops

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Improves IP address utilization
💡 VLSM allows subnet sizes to match actual requirements, reducing address wastage.

</details>

---

### 208. In the TCP/IP model, which layer ensures reliable data delivery through acknowledgments and retransmissions?

* [ ] Application
* [ ] Network
* [ ] Internet
* [ ] Transport

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Transport
💡 The Transport layer (TCP) provides reliability, sequencing, and flow control.

</details>

---

### 209. In Software-Defined Networking (SDN), which layer is responsible for making centralized, high-level traffic flow decisions?

* [ ] Infrastructure Layer
* [ ] Control Layer
* [ ] Application Layer
* [ ] Data Plane

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Control Layer
💡 The control layer acts as the SDN controller, managing forwarding behavior across devices.

</details>

---

### 210. Which of the following is **NOT** considered a core benefit of Software-Defined Networking (SDN) in enterprise environments?

* [ ] Centralized network control
* [ ] Vendor lock-in
* [ ] Network automation
* [ ] Programmability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Vendor lock-in
💡 SDN promotes vendor neutrality and open standards; vendor lock-in is a drawback of traditional networking, not a benefit of SDN.

</details>

---

### 211. Which routing protocol was originally **Cisco-proprietary** and later replaced by a more advanced and scalable protocol?

* [ ] OSPF
* [ ] RIP
* [ ] IGRP
* [ ] BGP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IGRP
💡 IGRP was Cisco-proprietary and classful; it was later replaced by EIGRP, which supports CIDR and VLSM.

</details>

---

### 212. Which Cisco IOS command provides a concise summary of interface status and assigned IP addresses?

* [ ] show running-config
* [ ] show ip interface brief
* [ ] show vlan
* [ ] show mac address-table

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** show ip interface brief
💡 This command quickly displays interface state, IP assignment, and protocol status—commonly used in troubleshooting.

</details>

---

### 213. Which protocol uses **UDP port 1812** to perform centralized authentication for network access?

* [ ] TACACS+
* [ ] RADIUS
* [ ] SSH
* [ ] HTTPS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RADIUS
💡 RADIUS uses UDP ports 1812 (authentication) and 1813 (accounting) and is widely used for network access control.

</details>

---

### 214. What is the functional impact of applying an **inbound ACL** on a router interface?

* [ ] Filters packets as they exit the interface
* [ ] Filters packets as they enter the interface
* [ ] Blocks all incoming traffic by default
* [ ] Performs NAT translation on packets

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Filters packets as they enter the interface
💡 Inbound ACLs inspect packets before routing decisions are made, reducing router processing overhead.

</details>

---

### 215. An organization uses private IPv4 addresses internally and wants to allow internet access without exposing internal IPs. Which NAT solution is most appropriate?

* [ ] Static NAT
* [ ] Port Address Translation (PAT)
* [ ] Dynamic NAT
* [ ] Proxy NAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Port Address Translation (PAT)
💡 PAT allows many internal hosts to share a single public IP using unique port numbers.

</details>

---

### 216. Multiple redundant links between switches are causing broadcast storms. Which protocol should be enabled to resolve this issue?

* [ ] OSPF
* [ ] VLAN
* [ ] STP
* [ ] PPP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** STP
💡 Spanning Tree Protocol prevents Layer-2 loops by blocking redundant paths while maintaining network redundancy.

</details>

---

### 217. Packets are being dropped between two routers running RIP, even though routing tables appear correct. What is the **most likely cause**?

* [ ] Subnet mask mismatch
* [ ] ACL blocking RIP updates
* [ ] Incorrect interface speed
* [ ] Duplicate MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Subnet mask mismatch
💡 RIP requires consistent subnet masks; mismatches can cause routing inconsistencies and dropped traffic.

</details>

---

### 218. A /30 subnet is configured between two routers, but communication is failing. What should be verified **first**?

* [ ] Whether RIP is enabled
* [ ] ACL configuration
* [ ] Host address assignment
* [ ] Routing protocol timers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Host address assignment
💡 A /30 subnet provides only two usable IPs; incorrect assignment can immediately break connectivity.

</details>

---

### 219. You are required to create **multiple broadcast domains** for different departments while using a single physical switch. Which technology is most appropriate?

* [ ] Subnetting
* [ ] Access Control Lists
* [ ] VLAN
* [ ] VTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLAN
💡 VLANs logically segment broadcast domains without requiring separate physical switches.

</details>

---

### 220. Which address class historically allowed up to **16 million hosts per network**, making it unsuitable for efficient IP utilization?

* [ ] Class A
* [ ] Class B
* [ ] Class C
* [ ] Class D

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Class A
💡 Class A networks support over 16 million hosts, leading to massive address wastage in classful addressing.

</details>

---

### 221. Which Ethernet media type is **most suitable for high-speed backbone connections** between switches over long distances?

* [ ] Cat5e
* [ ] Cat6
* [ ] Coaxial cable
* [ ] Fiber optic cable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fiber optic cable
💡 Fiber provides high bandwidth, low attenuation, and immunity to electromagnetic interference.

</details>

---

### 222. Which protocol enables routers to exchange **IPv6 routing information** using a link-state approach?

* [ ] RIP
* [ ] BGP
* [ ] OSPFv3
* [ ] ARP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OSPFv3
💡 OSPFv3 is specifically designed for IPv6 and operates independently of IPv4.

</details>

---

### 223. Which networking device operates strictly at the **Physical layer** and floods incoming signals to all ports?

* [ ] Switch
* [ ] Router
* [ ] Bridge
* [ ] Hub

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hub
💡 Hubs regenerate electrical signals without MAC learning, causing collisions and inefficiency.

</details>

---

### 224. Which Cisco IOS command ensures configuration changes persist after a reboot?

* [ ] write memory
* [ ] save file
* [ ] commit config
* [ ] reload config

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** write memory
💡 This command saves the running configuration to NVRAM as the startup configuration.

</details>

---

### 225. Which subnet mask provides **exactly 14 usable IPv4 host addresses**?

* [ ] 255.255.255.240 (/28)
* [ ] 255.255.255.248 (/29)
* [ ] 255.255.255.224 (/27)
* [ ] 255.255.255.192 (/26)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 255.255.255.240 (/28)
💡 A /28 subnet has 16 total addresses; subtracting network and broadcast leaves 14 usable hosts.

</details>

---

### 226. Which sequence correctly represents the **TCP three-way handshake**?

* [ ] SYN → ACK → ACK
* [ ] SYN → SYN-ACK → ACK
* [ ] ACK → SYN → ACK
* [ ] SYN-ACK → SYN → ACK

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SYN → SYN-ACK → ACK
💡 This process establishes a reliable TCP connection with synchronized sequence numbers.

</details>

---

### 227. Which portion of an IPv4 address uniquely identifies a device within its network?

* [ ] Subnet mask
* [ ] Host portion
* [ ] Network portion
* [ ] CIDR notation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Host portion
💡 The host portion differentiates individual devices within the same network ID.

</details>

---

### 228. Which routing protocol characteristic distinguishes OSPF from distance-vector protocols?

* [ ] Uses hop count as its metric
* [ ] Periodically sends full routing tables
* [ ] Maintains a link-state database and uses Dijkstra’s algorithm
* [ ] Does not support CIDR

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Maintains a link-state database and uses Dijkstra’s algorithm
💡 OSPF builds a complete topology map and calculates shortest paths using SPF.

</details>

---

### 229. In Cisco networking, which feature allows logical separation of networks while using the same physical infrastructure?

* [ ] Trunking
* [ ] Subnet masks
* [ ] VLANs
* [ ] NAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLANs
💡 VLANs provide logical isolation, improved security, and efficient broadcast control.

</details>

---

### 230. A company is migrating from a traditional network to a Software-Defined Networking (SDN) architecture. Which change most directly differentiates the SDN model from conventional network designs?

* [ ] Each network device independently makes routing and forwarding decisions
* [ ] Control logic is centralized and separated from the data forwarding plane
* [ ] VLANs are replaced entirely by virtual routing instances
* [ ] Network devices no longer require any routing protocols

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Control logic is centralized and separated from the data forwarding plane
💡 SDN fundamentally decouples the control plane from the data plane, allowing centralized controllers to manage traffic flows dynamically and programmatically—an essential distinction from traditional distributed network control.

</details>

---
