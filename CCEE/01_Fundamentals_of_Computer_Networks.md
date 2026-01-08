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

