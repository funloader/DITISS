> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

# SET 01 – Advanced Networking & Routing (DITISS Level)

---

### 1. Router R1 has a static route and a RIP-advertised route to the same network. Which route will R1 prefer?

* [ ] The route with the lowest hop count
* [ ] The static route
* [ ] The RIP route
* [ ] The route with the highest metric

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The static route
💡 Routers choose routes based on **Administrative Distance (AD)**. Static routes (AD = 1) are preferred over RIP routes (AD = 120).

</details>

---

### 2. RIPv2 uses which method to send updates to neighboring routers?

* [ ] Broadcast
* [ ] Multicast
* [ ] Unicast only
* [ ] Anycast

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multicast
💡 RIPv2 uses **multicast address 224.0.0.9** to send routing updates efficiently, reducing unnecessary load on hosts.

</details>

---

### 3. What is the **maximum hop count** that RIP considers as reachable?

* [ ] 15
* [ ] 16
* [ ] 30
* [ ] Unlimited

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 15
💡 RIP considers a network unreachable if the hop count exceeds 15.

</details>

---

### **4. Router R2 has received multiple OSPF LSAs but cannot form adjacency with R3. Which command helps verify Hello packet exchange?**

* [ ] show ip route
* [ ] show running-config
* [ ] ping
* [ ] debug ip ospf hello

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** debug ip ospf hello
💡 This command displays the **sending and receiving of OSPF Hello packets**, which are essential for forming adjacencies. If Hello packets are not exchanged, adjacency will fail.

</details>

---

### 5. Consider the command:

`router ospf 1`
`network 192.168.1.0 255.255.255.0 area 0`

What is wrong with this configuration?

* [ ] Incorrect Area ID
* [ ] Incorrect subnet mask
* [ ] Incorrect wild-card mask
* [ ] OSPF process number invalid

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Incorrect wild-card mask
💡 OSPF uses **wild-card masks** in the network command, not subnet masks. The correct command should use `0.0.0.255`.

</details>

---

### 6. A network has the following routes: Static (AD=1), RIP (AD=120), IGRP (AD=100). Which route will the router choose?

* [ ] RIP
* [ ] IGRP
* [ ] Static
* [ ] Route with lowest hop count

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Static
💡 Administrative Distance determines preference. Static routes (AD=1) are always preferred over IGRP (100) and RIP (120).

</details>

---

### 7. What is the **default update interval** for RIP?

* [ ] 30 seconds
* [ ] 60 seconds
* [ ] 90 seconds
* [ ] 180 seconds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 30 seconds
💡 RIP sends the full routing table to neighbors every **30 seconds**.

</details>

---

### 8. Which multicast address does RIPv2 use?

* [ ] 224.0.0.5
* [ ] 224.0.0.9
* [ ] 224.0.0.10
* [ ] 224.0.0.11

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 224.0.0.9
💡 This is the reserved multicast address for **RIPv2 updates**.

</details>

---

### **9. The wild-card mask `0.0.0.7` corresponds to which subnet?**

* [ ] /27
* [ ] /29
* [ ] /25
* [ ] /30

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /29
💡 Wildcard mask `0.0.0.7` has 3 variable bits (`0000 0111`). Subtracting from 32 bits total gives a /29 subnet (255.255.255.248).

</details>

---

### 10. Which routing protocol is **classless** and supports VLSM?

* [ ] RIP v1
* [ ] RIP v2
* [ ] IGRP
* [ ] None

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RIP v2
💡 RIP v2 supports **classless routing** and VLSM; RIP v1 is classful.

</details>

---

### 11. Loopback interfaces are primarily used for?

* [ ] Physical connectivity
* [ ] Logical testing and router ID assignment
* [ ] WAN interfaces
* [ ] Default gateway

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Logical testing and router ID assignment
💡 Loopbacks are **logical interfaces** and often used as OSPF router IDs or management interfaces.

</details>

---

### 12. What metric does RIP use to select the best path?

* [ ] Bandwidth
* [ ] Hop count
* [ ] Delay
* [ ] Cost

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hop count
💡 RIP chooses the path with the **lowest hop count**. Maximum 15 hops allowed.

</details>

---

### **13. Which routing protocol can handle multiple routed protocols such as IP, IPX, and AppleTalk?**

* [ ] RIP v1
* [ ] RIP v2
* [ ] OSPF
* [ ] EIGRP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EIGRP
💡 **EIGRP** is a multirouting protocol capable of supporting multiple routed protocols (IP, IPX, AppleTalk). RIP v1 and v2 only support IP.

</details>

---

### 14. Default holddown timer for RIP is?

* [ ] 120 seconds
* [ ] 180 seconds
* [ ] 240 seconds
* [ ] 300 seconds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 180 seconds
💡 Holddown prevents flapping routes from being reinstated too quickly.

</details>

---

### 15. Which command enables OSPF process 101 on a router?

* [ ] router 101
* [ ] router ospf 101
* [ ] ospf 101
* [ ] en 101

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** router ospf 101
💡 This is the correct IOS syntax to start an OSPF process.

</details>

---

### **16. What mechanism does RIP v2 use to send its routing table to neighbors?**

* [ ] Route broadcast (like RIP v1)
* [ ] Route multicast
* [ ] Route advertise (general term)
* [ ] None

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Route multicast
💡 RIP v2 sends routing updates using **multicast address 224.0.0.9**, unlike RIP v1 which uses broadcast.

</details>

---

### 17. What are essential for dynamic routing in a router?

* [ ] Routed protocols only
* [ ] Routing protocols only
* [ ] Both routed and routing protocols
* [ ] None

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both routed and routing protocols
💡 Routed protocols carry data; routing protocols exchange route info to populate routing tables.

</details>

---

### 18. Administrative distance (AD) is defined as an integer from?

* [ ] 0–255
* [ ] 1–255
* [ ] 0–256
* [ ] 1–256

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 0–255
💡 AD is used to determine trustworthiness of routes; 0 = most trusted, 255 = unusable.

</details>

---

### 19. Default AD of IGRP is?

* [ ] 90
* [ ] 100
* [ ] 110
* [ ] 120

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 100
💡 Cisco IGRP uses AD = 100 for its routes.

</details>

---

### 20. The command `ip route 0.0.0.0 0.0.0.0 170.10.11.1` is an example of?

* [ ] Static routing
* [ ] Default routing
* [ ] Dynamic routing
* [ ] Invalid command

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Default routing
💡 This is a static **default route**, directing traffic to the next-hop router if no specific route exists.

</details>

---

Perfect! I’ve carefully reviewed your original MCQs and I can now **upgrade them to PG-DITISS CCEE-level questions**. I will make them:

* **Scenario-based or analytical where possible**
* **One correct answer per question**
* **Distractors plausible and credible**
* **Formatted exactly as requested**

Here’s the fully improved set:

---

### 21. Which routing protocol supports discontiguous networks **without requiring manual summarization** by default?

* [ ] RIPv2
* [ ] EIGRP
* [ ] IGRP
* [ ] OSPF

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EIGRP
💡 EIGRP automatically supports discontiguous networks because it uses **classless routing** with VLSM and does not rely on summarization by default. RIPv2 also supports discontiguous networks but requires **manual summarization** configuration.

</details>

---

### 22. To view the complete routing table on a Cisco router, which command should be used?

* [ ] show route table
* [ ] show route
* [ ] show ip route
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** show ip route
💡 The `show ip route` command displays all routes in the routing table, including connected, static, and learned routes.

</details>

---

### 23. EIGRP uses multiple metrics to determine the **best path**. Which of the following are included in its primary metric calculation?

* [ ] Delay
* [ ] Reliability
* [ ] Bandwidth
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above  
💡 EIGRP computes a **composite metric** primarily using **bandwidth, delay, reliability, and load**. MTU is exchanged in routing updates but **does not affect metric calculation**. The best path is chosen based on the lowest metric value.

</details>

---

### 24. Auto-summarization is **disabled by default** in which routing protocol?

* [ ] RIPv1
* [ ] RIPv2
* [ ] OSPF
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RIPv2
💡 RIPv1 performs auto-summarization by default (classful), while RIPv2 is **classless** and does **not auto-summarize**, supporting VLSM and discontiguous networks. OSPF is inherently classless.

</details>

---

### 25. Hierarchical network design, including core, distribution, and access layers, is a characteristic of which protocol type?

* [ ] RIPv1
* [ ] RIPv2
* [ ] OSPF
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OSPF
💡 OSPF is designed for **hierarchical IP routing**, supporting **areas** and efficient routing in large networks. RIPv1 and RIPv2 are flat and do not implement hierarchical structure.

</details>

---

### 26. What uniquely identifies a router in an OSPF network?

* [ ] Interface IP address
* [ ] Router ID
* [ ] MAC address
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Router ID  
💡 OSPF uses a **Router ID (RID)**, a 32-bit logical identifier, to uniquely identify routers in the network. It is typically set manually or automatically chosen as the **highest IP address on a loopback or active interface**. It is **not tied directly to any single interface IP**.

</details>

---

### 27. How long is an IPv6 address?

* [ ] 32 bits
* [ ] 128 bytes
* [ ] 64 bits
* [ ] 128 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 128 bits
💡 IPv6 addresses are **128-bit identifiers**, written in hexadecimal notation, supporting a vastly larger address space than IPv4.

</details>

---

### 28. Which command is used to save the current running configuration to startup configuration on a Cisco device?

* [ ] copy running backup
* [ ] copy running-config startup-config
* [ ] config mem
* [ ] wr mem

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** copy running-config startup-config
💡 This command saves the **active running configuration** to NVRAM so that it persists after a reboot.

</details>

---

### 29. To delete the configuration stored in NVRAM, which command is correct?

* [ ] erase startup
* [ ] erase nvram
* [ ] delete nvram
* [ ] erase running

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** erase startup
💡 `erase startup-config` clears the saved configuration from NVRAM, leaving the router with no startup configuration.

</details>

---

### 30. Which protocols are used to configure **trunking** on a switch?

* [ ] VLAN Trunking Protocol (VTP) only
* [ ] 802.1Q and ISL
* [ ] Both VTP and trunking protocols
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 802.1Q and ISL  
💡 **802.1Q** (IEEE standard) and **ISL** (Cisco proprietary) are the protocols used for **trunking**, carrying multiple VLANs over a single link. **VTP is not a trunking protocol**; it only propagates VLAN information across switches.

</details>

---

### 31. What is the **fundamental purpose** of a computer network?

* [ ] Sharing resources
* [ ] Storing data
* [ ] Performing calculations
* [ ] Enhancing security

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Sharing resources
💡 Networks primarily exist to **allow multiple devices to share resources**, such as files, printers, and internet access.

</details>

---

### 32. Which topology does the **Internet resemble**, due to multiple redundant paths?

* [ ] Ring
* [ ] Bus
* [ ] Star
* [ ] Mesh

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mesh
💡 The Internet is a **mesh topology** at a large scale, with multiple interconnections ensuring redundancy and resilience.

</details>

---

### 33. Which type of network spans a large geographical area, like a city, country, or the world?

* [ ] LAN
* [ ] MAN
* [ ] WAN
* [ ] PAN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** WAN
💡 WANs connect multiple LANs over **large distances**, unlike LANs (local) or PANs (personal). MAN is city-scale.

</details>

---

### 34. Which device connects **different network segments** and routes traffic between them?

* [ ] Repeater
* [ ] Router
* [ ] Bridge
* [ ] Modem

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Router
💡 Routers forward packets **between networks** based on IP addresses, unlike repeaters (physical layer) or bridges (link layer).

</details>

---

### 35. The first wide-area packet-switched network in the US was called:

* [ ] CNNET
* [ ] NSFNET
* [ ] ASAPNET
* [ ] ARPANET

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ARPANET
💡 ARPANET, launched in 1969, was the **precursor to the modern Internet**, connecting universities and research institutions.

</details>

---

### 36. The combination of two or more interconnected networks is called:

* [ ] Internetwork
* [ ] LAN
* [ ] MAN
* [ ] WAN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Internetwork
💡 An **internetwork** is formed when multiple networks are connected using routers or gateways.

</details>

---

### 37. ISP stands for:

* [ ] International Service Provider
* [ ] International System Provider
* [ ] Internet Service Provider
* [ ] Internetwork System Provider

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Internet Service Provider
💡 ISPs provide **internet access** to organizations and individuals.

</details>

---

### 38. National ISPs interconnect at which points for exchanging traffic?

* [ ] Peering Points
* [ ] Network Access Points (NAPs) / Internet Exchange Points (IXPs)
* [ ] National ISP
* [ ] None of these

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Access Points (NAPs) / Internet Exchange Points (IXPs)  
💡 Historically, **NAPs** were used for ISPs to exchange traffic. Modern networks also use **IXPs** to interconnect ISPs efficiently. These points form the backbone for national and global internet traffic exchange.

</details>

---

### 39. Which network typically provides **high-speed transmission** within a limited area?

* [ ] MAN
* [ ] LAN
* [ ] WAN
* [ ] Internetwork

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** LAN
💡 LANs support **high-speed connectivity** (Ethernet, Wi-Fi) within offices or buildings, unlike WANs which are slower over large distances.

</details>

---

### 40. Data transmission where both directions are possible, but only **one direction at a time**, is called:

* [ ] Simplex
* [ ] Four-wire circuit
* [ ] Half-duplex
* [ ] Full duplex

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Half-duplex
💡 In half-duplex communication, **devices take turns** sending data. Full-duplex allows simultaneous transmission.

</details>

---

