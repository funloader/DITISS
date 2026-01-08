> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

# SET 02 – Interior Gateway Routing Protocol & Software-Defined Networking (SDN) (DITISS Level)

---

### 1. A network administrator observes that routes learned via OSPF are preferred over RIP routes but not over EIGRP routes. Which administrative distance value of OSPF explains this behavior?

* [ ] 90
* [ ] 100
* [ ] 110
* [ ] 120

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 110
💡 OSPF has an administrative distance of 110, which is lower than RIP (120) but higher than EIGRP (90), explaining the observed route preference.

</details>

---

### **Q2. In EIGRP, where are successor routes that satisfy the feasibility condition stored for quick convergence?**

* [ ] In the routing table only
* [ ] In the neighbor table only
* [ ] In the topology table only
* [ ] In the topology table (with the best successor copied to the routing table)

**✅ Correct Answer:** In the topology table (with the best successor copied to the routing table)

💡 EIGRP stores **all successors and feasible successors in the topology table**.
Only the **best successor** is installed in the routing table, while others remain as backups for fast convergence.

---

### 3. An enterprise uses OSPF for large-scale routing. Which routing algorithm enables OSPF to compute the shortest path efficiently?

* [ ] Distance-vector
* [ ] Link-state
* [ ] Path-vector
* [ ] Hybrid

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Link-state
💡 OSPF is a link-state protocol that uses Dijkstra’s SPF algorithm to calculate shortest paths based on link cost.

</details>

---

### 4. Which algorithm allows EIGRP to achieve fast convergence without routing loops?

* [ ] SPF
* [ ] DUAL
* [ ] Bellman-Ford
* [ ] Dijkstra’s

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DUAL
💡 Diffusing Update Algorithm (DUAL) ensures loop-free and rapid convergence in EIGRP.

</details>

---

### 5. Which Cisco IOS command displays all EIGRP successor and feasible successor routes?

* [ ] show ip route eigrp
* [ ] show ip eigrp summary
* [ ] show ip eigrp topology
* [ ] show ip eigrp neighbors

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** show ip eigrp topology
💡 This command displays all routes known to EIGRP, including successors and feasible successors.

</details>

---

### 6. Which routing protocol limits the maximum hop count to 15, making it unsuitable for large networks?

* [ ] RIPv1
* [ ] RIPv2
* [ ] EIGRP
* [ ] Both RIPv1 and RIPv2

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both RIPv1 and RIPv2
💡 RIP uses hop count as its metric, with 15 as the maximum reachable distance.

</details>

---

### 7. By default, how frequently does a RIPv1 router broadcast its entire routing table?

* [ ] Every 30 seconds
* [ ] Every 60 seconds
* [ ] Every 90 seconds
* [ ] Only on topology change

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Every 30 seconds
💡 RIP periodically broadcasts full routing updates every 30 seconds, contributing to higher bandwidth usage.

</details>

---

### **Q8. Which command allows a network engineer to view real-time RIP routing updates?**

* [ ] show ip route
* [ ] debug ip rip
* [ ] show ip protocols
* [ ] debug ip route

**✅ Correct Answer:** debug ip rip

💡 This command displays RIP update advertisements sent and received by the router.
⚠️ *Debug commands are CPU-intensive and should be used cautiously, especially on production routers.*


---

### 9. While debugging RIP, a router receives an update for network 172.16.10.0 with a metric of 16. What does this indicate?

* [ ] The route is 16 hops away
* [ ] The route has excessive delay
* [ ] The route is unreachable
* [ ] The route is congested

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The route is unreachable
💡 In RIP, a hop count of 16 represents infinity, meaning the destination network is unreachable.

</details>

---

### 10. What is the default administrative distance of a static route?

* [ ] 0
* [ ] 1
* [ ] 90
* [ ] 100

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1
💡 Static routes have an AD of 1 by default, making them highly preferred unless manually altered.

</details>

---

### 11. Which protocol sends a complete routing table update every 30 seconds?

* [ ] EIGRP
* [ ] RIP
* [ ] ICMP
* [ ] IP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RIP
💡 RIP periodically sends full routing table updates rather than incremental updates.

</details>

---

### 12. What is the default administrative distance of RIP?

* [ ] 0
* [ ] 90
* [ ] 120
* [ ] 130

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 120
💡 RIP has a higher AD, making it less preferred compared to OSPF or EIGRP.

</details>

---

### 13. In which scenario is default routing most appropriate?

* [ ] Stub networks with a single exit path
* [ ] Networks with multiple exit paths
* [ ] Large enterprise core networks
* [ ] Fully meshed WANs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Stub networks with a single exit path
💡 Default routing minimizes routing table size and complexity in stub networks.

</details>

---

### Q14. In EIGRP communication, which packet type is commonly multicast during normal operation but may be unicast for reliable delivery?

* [ ] Query
* [ ] ACK
* [ ] Update
* [ ] Reply

**✅ Correct Answer:** Update

💡 EIGRP Update packets are multicast during routine operation and unicast during retransmissions or when reliable delivery to a specific neighbor is required.

---

### Q15. Which EIGRP packet type is sent strictly as unicast?

* [ ] Reply
* [ ] Hello
* [ ] Update
* [ ] Query

**✅ Correct Answer:** Reply

💡 EIGRP Reply packets are **always sent as unicast** and **must be acknowledged**, ensuring reliable, loop-free convergence in the DUAL algorithm.

---

### Q16. Does EIGRP use hop count as part of its metric calculation?

* [ ] Yes
* [ ] No
* [ ] Only when configured
* [ ] Only in IPv6

**✅ Correct Answer:** No

💡 EIGRP uses **bandwidth and delay by default**, with optional reliability, load, and MTU.
While EIGRP **tracks hop count internally for loop prevention**, it **does not use hop count in metric calculation**.

---

### 17. Where does EIGRP maintain the list of feasible successors?

* [ ] Routing table
* [ ] Neighbor table
* [ ] Topology table
* [ ] Link-state database

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Topology table
💡 The topology table stores all learned routes that satisfy the feasibility condition.

</details>

---

### Q18. What is the default maximum hop count supported by IGRP?

* [ ] 255
* [ ] 256
* [ ] 100
* [ ] No limit

**✅ Correct Answer:** 255

💡 IGRP supports a maximum hop count of **255**, allowing larger networks than RIP.
⚠️ *IGRP is obsolete and no longer supported on modern Cisco IOS, having been replaced by EIGRP.*

---

### 19. Which routing protocol is Cisco-proprietary and distance-vector in nature?

* [ ] OSPF
* [ ] RIPv2
* [ ] IGRP
* [ ] BGP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IGRP
💡 IGRP is a Cisco-proprietary distance-vector protocol, now obsolete and replaced by EIGRP.

</details>

---

### 20. Which routing protocol supports Variable Length Subnet Masking (VLSM)?

* [ ] RIPv2
* [ ] RIPv1
* [ ] Both RIPv1 and RIPv2
* [ ] Neither

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RIPv2
💡 RIPv2 is classless and carries subnet mask information, enabling VLSM.

</details>

---

### 21. In modern enterprise and cloud networks, what does the term *Software-Defined Networking (SDN)* precisely refer to?

* [ ] Software tools used for automated network testing
* [ ] A proprietary networking hardware architecture
* [ ] A network architecture that decouples the control plane from the data plane
* [ ] A secure protocol for encrypted network communication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A network architecture that decouples the control plane from the data plane
💡 SDN introduces architectural separation where control logic is centralized in software controllers, enabling programmability and dynamic control—core to SDN as defined by ONF.

</details>

---

### 22. What is the *primary architectural motivation* behind separating the control plane from the data plane in SDN?

* [ ] To reduce hardware manufacturing costs
* [ ] To enhance scalability, programmability, and centralized policy enforcement
* [ ] To eliminate routing protocols from networks
* [ ] To increase packet forwarding speed at switches

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To enhance scalability, programmability, and centralized policy enforcement
💡 Separation enables centralized intelligence, simplified device logic, faster innovation, and flexible policy-based network management.

</details>

---

### 23. Which protocol is most commonly used as a *southbound interface* for communication between an SDN controller and forwarding devices?

* [ ] SNMP
* [ ] OpenFlow
* [ ] HTTP/REST
* [ ] ICMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OpenFlow
💡 OpenFlow, standardized by ONF, allows controllers to manage flow tables in switches, making it the most widely referenced SDN southbound protocol.

</details>

---

### 24. In an SDN architecture, what is the **core responsibility** of the SDN controller?

* [ ] Forwarding packets at line speed
* [ ] Acting as a physical routing device
* [ ] Centralized control, policy enforcement, and traffic decision-making
* [ ] Providing network address translation (NAT) services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centralized control, policy enforcement, and traffic decision-making
💡 The controller maintains a global network view and programs forwarding behavior across devices.

</details>

---

### 25. Which of the following is **NOT** a recognized advantage of adopting SDN in large-scale networks?

* [ ] Enhanced automation and programmability
* [ ] Improved network visibility and control
* [ ] Decreased network flexibility
* [ ] Rapid provisioning of network services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Decreased network flexibility
💡 SDN explicitly improves flexibility by enabling dynamic reconfiguration via software.

</details>

---

### 26. An **SDN application** is best described as:

* [ ] Firmware installed on network switches
* [ ] A virtualization layer for routing devices
* [ ] Software running on the SDN controller to implement network services
* [ ] A hardware accelerator for packet processing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Software running on the SDN controller to implement network services
💡 SDN applications use northbound APIs to define policies such as routing, QoS, firewalling, and load balancing.

</details>

---

### 27. From an architectural abstraction perspective, SDN control logic and orchestration are most closely associated with which OSI layer?

* [ ] Physical Layer
* [ ] Data Link Layer
* [ ] Network Layer
* [ ] Application Layer

✅ **Correct Answer:** Application Layer
💡 SDN does not strictly map to OSI layers, but controllers and SDN applications function as application-layer software that abstracts and controls lower-layer network behavior.

---

### 28. Which organization is primarily responsible for standardizing and promoting OpenFlow?

* [ ] Cisco Systems
* [ ] IEEE
* [ ] Open Networking Foundation (ONF)
* [ ] IETF

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Open Networking Foundation (ONF)
💡 ONF is the industry consortium driving SDN and OpenFlow standardization.

</details>

---

### 29. Which of the following is **NOT** a typical SDN use case?

* [ ] Network virtualization and multi-tenancy
* [ ] Dynamic QoS enforcement
* [ ] Software-defined storage management
* [ ] Network analytics and traffic engineering

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Software-defined storage management
💡 While related conceptually, software-defined storage is outside the primary scope of SDN.

</details>

---

### 30. In SDN terminology, what is the *data plane* responsible for?

* [ ] Centralized routing decisions
* [ ] Managing security policies
* [ ] Packet processing and forwarding based on flow rules
* [ ] Controller-to-controller synchronization

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Packet processing and forwarding based on flow rules
💡 The data plane executes forwarding decisions programmed by the control plane.

</details>

---

### 31. In an SDN-based network, which component is primarily responsible for *computing and installing forwarding rules* in switches?

* [ ] SDN switch
* [ ] SDN controller
* [ ] SDN application
* [ ] Virtual router

✅ **Correct Answer:** SDN controller
💡 SDN applications define *what* the network should do, but the controller computes paths and installs flow rules into switches.

---

### 32. Which of the following is **NOT** a commonly used SDN controller platform?

* [ ] OpenDaylight
* [ ] Floodlight
* [ ] Ryu
* [ ] Cisco IOS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Cisco IOS
💡 Cisco IOS is a traditional network operating system, not an SDN controller.

</details>

---

### 33. What is the purpose of a **Northbound API** in SDN?

* [ ] Communication between switches
* [ ] Controller-to-controller synchronization
* [ ] Application-to-controller interaction
* [ ] Hardware abstraction for ASICs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Application-to-controller interaction
💡 Northbound APIs allow SDN applications to define network behavior abstractly.

</details>

---

### 34. In SDN and 5G networks, *network slicing* refers to:

* [ ] Physical segmentation of fiber cables
* [ ] Logical partitioning of network resources for different services
* [ ] Creation of backup routing paths
* [ ] Encryption of SDN control traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Logical partitioning of network resources for different services
💡 Network slicing enables multiple virtual networks with distinct QoS characteristics over shared infrastructure.

</details>

---

### 35. In SDN architecture, what best describes the **physical network infrastructure**?

* [ ] Control plane
* [ ] Application plane
* [ ] Data plane
* [ ] Management plane

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data plane
💡 Switches and routers forming the forwarding fabric belong to the data plane.

</details>

---

### 36. What is the **primary objective** of SDN adoption in modern networks?

* [ ] Elimination of physical networking devices
* [ ] Centralized control and increased programmability
* [ ] Replacement of IP routing
* [ ] Exclusive use of virtual networks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centralized control and increased programmability
💡 SDN simplifies network management and enables rapid innovation.

</details>

---

### 37. Which of the following is **NOT** a benefit commonly associated with SDN?

* [ ] Centralized management
* [ ] Improved scalability
* [ ] Reduced operational complexity
* [ ] Increased power consumption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Increased power consumption
💡 SDN typically improves efficiency rather than increasing power usage.

</details>

---

### 38. In the context of SDN, **network virtualization** refers to:

* [ ] Creating VLANs using switch configuration
* [ ] Virtualizing physical network resources into multiple logical networks
* [ ] Deploying hypervisors on routers
* [ ] Implementing only software firewalls

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtualizing physical network resources into multiple logical networks
💡 SDN enables abstraction and isolation of network resources for multi-tenant environments.

</details>

---

### 39. One of the major scalability challenges in SDN arises because:

* [ ] Switches cannot process packets at line rate
* [ ] Centralized controllers may become performance bottlenecks
* [ ] SDN eliminates distributed routing entirely
* [ ] OpenFlow does not support large networks

✅ **Correct Answer:** Centralized controllers may become performance bottlenecks
💡 Large-scale SDN deployments often use distributed or hierarchical controllers to address scalability and fault tolerance.

---

### 40. Which statement best distinguishes **SDN** from **NFV (Network Functions Virtualization) ?

* [ ] SDN focuses on virtualizing hardware, while NFV focuses on packet forwarding
* [ ] SDN manages control and forwarding behavior, while NFV virtualizes network functions like firewalls and load balancers
* [ ] NFV replaces SDN controllers
* [ ] SDN and NFV are identical concepts

✅ **Correct Answer:** SDN manages control and forwarding behavior, while NFV virtualizes network functions like firewalls and load balancers
💡 SDN and NFV are complementary: SDN controls traffic flows, while NFV runs network services as software on virtualized infrastructure.

---
