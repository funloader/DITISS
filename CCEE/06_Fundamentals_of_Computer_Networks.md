> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---
# 200 MCQ Set

---

### 1. A network administrator configures a static route on a router. Which of the following is a characteristic of static routing in this context?

* [ ] Automatically adapts to network topology changes
* [ ] Requires manual configuration and maintenance
* [ ] Consumes additional bandwidth for updates
* [ ] Is primarily used in large, dynamic networks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Requires manual configuration and maintenance
💡 Static routes must be manually configured and do not adapt to network changes automatically. They are commonly used in small networks or for controlling specific paths.

</details>

---

### 2. On a Cisco router, which command correctly configures a static route to network 192.168.20.0/24 via next-hop 10.0.0.2?

* [ ] `set static-route 192.168.20.0 255.255.255.0 10.0.0.2`
* [ ] `ip routing 192.168.20.0 255.255.255.0 10.0.0.2`
* [ ] `ip route 192.168.20.0 255.255.255.0 10.0.0.2`
* [ ] `route static 192.168.20.0 10.0.0.2`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `ip route 192.168.20.0 255.255.255.0 10.0.0.2`
💡 Cisco IOS uses the `ip route [DESTINATION] [MASK] [NEXT-HOP]` command to configure static routes.

</details>

---

### 3. If a static route's next-hop becomes unreachable but the interface remains up, what happens to the route in the routing table?

* [ ] It is automatically replaced by another route
* [ ] It is removed from the routing table
* [ ] It remains in the routing table but packets are dropped
* [ ] The router reboots

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It remains in the routing table but packets are dropped
💡 Static routes do not self-heal. If the next-hop is unreachable, the route persists until manually removed, but traffic cannot be forwarded.

</details>

---

### 4. A network engineer wants to implement a protocol that can automatically adjust to network changes. Which of the following is a dynamic routing protocol suitable for this purpose?

* [ ] SSH
* [ ] DHCP
* [ ] RIP
* [ ] DNS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RIP
💡 RIP is a distance-vector dynamic routing protocol that periodically shares routing updates, allowing routers to adapt to network topology changes.

</details>

---

### 5. What is the default administrative distance (AD) of a static route on Cisco routers?

* [ ] 90
* [ ] 110
* [ ] 120
* [ ] 1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1
💡 Administrative distance indicates the trustworthiness of a route; static routes have the highest trust by default (AD = 1).

</details>

---

### 6. Which scenario demonstrates a key advantage of dynamic routing over static routing?

* [ ] Manually configuring all routes in a small office network
* [ ] Automatically adapting to network failures in large, multi-router environments
* [ ] Avoiding bandwidth usage on point-to-point links
* [ ] Using minimal memory for routing tables

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Automatically adapting to network failures in large, multi-router environments
💡 Dynamic routing protocols detect topology changes and adjust routing tables, reducing administrative overhead and improving reliability.

</details>

---

### 7. A router receives a packet destined for another network. Which of the following best describes the process of routing in this context?

* [ ] Encrypting the packet for security
* [ ] Forwarding the packet between different networks based on the routing table
* [ ] Translating IP addresses to MAC addresses
* [ ] Assigning MAC addresses to hosts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forwarding the packet between different networks based on the routing table
💡 Routing is the process of selecting paths and forwarding packets from source to destination across networks.

</details>

---

### 8. In a multi-protocol environment, administrative distance (AD) is used to:

* [ ] Determine the version of a routing protocol
* [ ] Select the preferred route when multiple protocols provide the same destination
* [ ] Compute the cost metric for OSPF
* [ ] Trigger routing table updates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Select the preferred route when multiple protocols provide the same destination
💡 Lower AD values are preferred. For example, static routes (AD=1) are preferred over RIP (AD=120).

</details>

---

### 9. Which routing protocol uses hop count as its metric and limits routes to a maximum of 15 hops?

* [ ] OSPF
* [ ] BGP
* [ ] RIP
* [ ] EIGRP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RIP
💡 RIP is a distance-vector protocol that measures path cost in hops. A hop count of 16 is considered unreachable.

</details>

---

### 10. When configuring a static route, the exit interface parameter specifies:

* [ ] The IP address of the destination network
* [ ] The next-hop router IP address
* [ ] The local interface used to forward packets
* [ ] The source IP for outgoing packets

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The local interface used to forward packets
💡 The exit interface tells the router which physical or logical interface to use for sending traffic toward the destination.

</details>

---

### 11. A network uses OSPF for routing. Which type of routing protocol is OSPF classified as?

* [ ] Distance-vector
* [ ] Link-state
* [ ] Path-vector
* [ ] Hybrid

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Link-state
💡 OSPF is a link-state protocol that builds a complete map of the network and uses Dijkstra’s SPF algorithm to calculate shortest paths.

</details>

---

### 12. Which protocol is designed to exchange routing information between different autonomous systems?

* [ ] RIP
* [ ] OSPF
* [ ] BGP
* [ ] EIGRP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** BGP
💡 BGP is a path-vector protocol used for inter-AS routing in large-scale networks, such as the Internet.

</details>

---

### 13. Which command in Cisco IOS displays routing protocols and their configurations?

* [ ] `show ip protocols`
* [ ] `show routing updates`
* [ ] `show updates`
* [ ] `debug ip route`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `show ip protocols`
💡 This command shows active routing protocols, timers, networks advertised, and administrative distances.

</details>

---

### 14. Which type of route is automatically created for networks directly connected to a router interface?

* [ ] Static route
* [ ] Default route
* [ ] Dynamic route
* [ ] Connected route

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Connected route
💡 Directly connected networks are automatically inserted into the routing table as connected routes with the local interface as the exit.

</details>

---

### 15. In RIP, what is the maximum number of hops allowed before a network is considered unreachable?

* [ ] 10
* [ ] 15
* [ ] 16
* [ ] 255

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 15
💡 RIP considers any route with a hop count of 16 as unreachable, limiting network size.

</details>

---

### 16. How frequently does RIP send periodic updates by default?

* [ ] Every 30 seconds
* [ ] Every 10 seconds
* [ ] On topology changes only
* [ ] Every 5 seconds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Every 30 seconds
💡 RIP broadcasts or multicasts updates every 30 seconds to maintain consistent routing tables.

</details>

---

### 17. A routing loop occurs when:

* [ ] A static route is misconfigured
* [ ] A link repeatedly goes up and down
* [ ] Packets circulate endlessly between routers
* [ ] A cable is incorrectly connected

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Packets circulate endlessly between routers
💡 Routing loops cause packets to circulate without reaching the destination, often due to inconsistent routing information.

</details>

---

### 18. If two routes to the same destination have different administrative distances, which one is selected?

* [ ] Both are installed
* [ ] The route with higher AD
* [ ] The route with lower AD
* [ ] Neither is used

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The route with lower AD
💡 AD represents route trustworthiness; the route with the lowest AD is preferred and installed in the routing table.

</details>

---

### 19. OSPF uses which metric to calculate the best path?

* [ ] Hop count
* [ ] Delay
* [ ] Bandwidth (Cost)
* [ ] Reliability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bandwidth (Cost)
💡 OSPF cost is inversely proportional to interface bandwidth. Lower-cost paths are preferred.

</details>

---

### 20. Which statement correctly describes a default route?

* [ ] Used only in static routing
* [ ] Not propagated by any routing protocol
* [ ] Matches all destination addresses not explicitly in the routing table
* [ ] Requires a dynamic routing protocol to function

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Matches all destination addresses not explicitly in the routing table
💡 A default route acts as a “gateway of last resort” for packets without a more specific match.

</details>

---

### 21. Which routing protocol supports unequal-cost load balancing?

* [ ] RIP
* [ ] EIGRP
* [ ] OSPF
* [ ] IS-IS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EIGRP
💡 EIGRP can perform unequal-cost load balancing using the variance command, unlike OSPF or RIP.

</details>

---

### 22. In EIGRP, a feasible successor is:

* [ ] The active route being used
* [ ] A backup route satisfying the feasibility condition
* [ ] A static route
* [ ] The default gateway of the router

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A backup route satisfying the feasibility condition
💡 Feasible successors are precomputed backup routes that are guaranteed loop-free.

</details>

---

### 23. How does OSPF prevent routing loops within an area?

* [ ] Using hop count
* [ ] Split horizon
* [ ] DUAL algorithm
* [ ] SPF algorithm with Link-State Advertisements (LSAs)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SPF algorithm with Link-State Advertisements (LSAs)
💡 OSPF builds a topology map and computes loop-free paths using Dijkstra’s Shortest Path First algorithm.

</details>

---

### 24. BGP path attributes are primarily used to:

* [ ] Encrypt routing tables
* [ ] Influence path selection
* [ ] Filter MAC addresses
* [ ] Configure IP addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Influence path selection
💡 Attributes like AS_PATH, MED, and LOCAL_PREF allow BGP to select the best route among multiple options.

</details>

---

### 25. Which command advertises static routes into RIP?

* [ ] `redistribute static`
* [ ] `static advertise`
* [ ] `route publish`
* [ ] `ip rip static`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `redistribute static`
💡 Redistribution allows static routes to be advertised by dynamic protocols like RIP.

</details>

---

### 26. The main function of a Designated Router (DR) in OSPF is to:

* [ ] Encrypt routing tables
* [ ] Manage subnet masks
* [ ] Reduce OSPF traffic on multi-access networks
* [ ] Block unnecessary updates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduce OSPF traffic on multi-access networks
💡 DR centralizes LSA exchange on broadcast networks, minimizing the number of adjacencies.

</details>

---

### 27. Which routing protocol uses TCP as its transport mechanism?

* [ ] RIP
* [ ] OSPF
* [ ] EIGRP
* [ ] BGP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** BGP
💡 BGP uses TCP port 179 to establish reliable peer connections between routers.

</details>

---

### 28. Which of the following is a classless routing protocol?

* [ ] RIPv1
* [ ] IGRP
* [ ] EIGRP
* [ ] BGPv3

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EIGRP
💡 Classless protocols support variable-length subnet masks (VLSM) and advertise subnet information. RIPv1 and IGRP are classful.

</details>

---

### 29. In BGP, which path attribute indicates the originating autonomous system?

* [ ] Weight
* [ ] Origin
* [ ] AS_PATH
* [ ] MED

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AS_PATH
💡 AS_PATH lists all autonomous systems a route has traversed, helping prevent loops and influence routing decisions.

</details>

---

### 30. A stub network in routing terminology refers to:

* [ ] A network with multiple exit paths
* [ ] A network that does not advertise routes
* [ ] A network with only one route in and out
* [ ] A loopback-only interface

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A network with only one route in and out
💡 Stub networks simplify routing by having a single exit path, reducing the size of routing tables.

</details>

---

### 31. What is the default administrative distance of IGRP on Cisco routers?

* [ ] 110
* [ ] 120
* [ ] 100
* [ ] 90

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 100
💡 IGRP is a Cisco proprietary distance-vector protocol with a default AD of 100, making it less preferred than static routes (AD 1).

</details>

---

### 32. Which routing protocol uses the DUAL (Diffusing Update Algorithm) to calculate loop-free paths?

* [ ] RIP
* [ ] IGRP
* [ ] EIGRP
* [ ] OSPF

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EIGRP
💡 EIGRP uses DUAL to calculate the best path and maintain feasible successors for backup routes, ensuring fast convergence and loop prevention.

</details>

---

### 33. What is the maximum hop count allowed in IGRP?

* [ ] 15
* [ ] 100
* [ ] 255
* [ ] 224

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 255
💡 IGRP uses a maximum hop count of 255, making it more suitable for larger networks compared to RIP (max 15).

</details>

---

### 34. Which protocol is classified as link-state rather than distance-vector?

* [ ] IGRP
* [ ] EIGRP
* [ ] OSPF
* [ ] RIP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OSPF
💡 OSPF builds a complete topology map of the network and uses the SPF algorithm, unlike distance-vector protocols which rely on hop count.

</details>

---

### 35. Which address type does OSPF use to send Hello packets on broadcast networks?

* [ ] Broadcast
* [ ] Unicast
* [ ] Multicast
* [ ] Anycast

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multicast
💡 OSPF uses multicast addresses 224.0.0.5 (all OSPF routers) and 224.0.0.6 (all DR/BDR routers) to exchange Hello packets efficiently.

</details>

---

### 36. Which of the following is a Cisco proprietary routing protocol?

* [ ] OSPF
* [ ] EIGRP
* [ ] BGP
* [ ] IS-IS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EIGRP
💡 EIGRP is Cisco proprietary and supports features like unequal-cost load balancing and DUAL-based loop-free routing.

</details>

---

### 37. What is the default administrative distance of OSPF?

* [ ] 90
* [ ] 100
* [ ] 110
* [ ] 120

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 110
💡 OSPF has a default AD of 110, which determines its preference relative to other protocols in the routing table.

</details>

---

### 38. What multicast address does EIGRP use to send routing updates?

* [ ] 224.0.0.5
* [ ] 224.0.0.6
* [ ] 224.0.0.9
* [ ] 224.0.0.10

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 224.0.0.10
💡 EIGRP multicasts updates to 224.0.0.10 to reach all EIGRP neighbors efficiently without flooding the network.

</details>

---

### 39. Which algorithm does OSPF use to compute the shortest path?

* [ ] Bellman-Ford
* [ ] DUAL
* [ ] SPF (Dijkstra)
* [ ] Split Horizon

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SPF (Dijkstra)
💡 OSPF uses Dijkstra’s Shortest Path First algorithm to compute loop-free routes based on link-state information.

</details>

---

### 40. On a broadcast network, what is the role of a Designated Router (DR) in OSPF?

* [ ] Resolve static routes
* [ ] Maintain neighbor tables and reduce adjacency count
* [ ] Assign IP addresses
* [ ] Encrypt routing tables

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Maintain neighbor tables and reduce adjacency count
💡 DR centralizes LSA exchanges on multi-access networks, reducing the number of required neighbor relationships.

</details>

---

### 41. Which command enables EIGRP for a specific autonomous system in Cisco IOS?

* [ ] `router eigrp [AS-number]`
* [ ] `eigrp enable [AS-number]`
* [ ] `eigrp start [AS-number]`
* [ ] `router enable eigrp`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `router eigrp [AS-number]`
💡 This command enters EIGRP configuration mode for the specified AS number on a Cisco router.

</details>

---

### 42. Which metric does EIGRP use by default to determine the best path?

* [ ] Hop count
* [ ] Bandwidth and delay
* [ ] Load and reliability
* [ ] MTU and cost

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bandwidth and delay
💡 EIGRP calculates its composite metric using bandwidth and delay by default; load and reliability are optional factors.

</details>

---

### 43. Which of the following is not a valid OSPF area type?

* [ ] Backbone area
* [ ] Stub area
* [ ] NSSA
* [ ] Core area

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Core area
💡 Valid OSPF areas include backbone (Area 0), stub, totally stubby, and NSSA. “Core area” is not an OSPF designation.

</details>

---

### 44. What is the default OSPF Hello interval on a broadcast network?

* [ ] 5 seconds
* [ ] 10 seconds
* [ ] 30 seconds
* [ ] 60 seconds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 10 seconds
💡 Hello packets are sent every 10 seconds on broadcast networks to establish and maintain neighbor adjacencies.

</details>

---

### 45. What is the function of the `network` command in EIGRP configuration?

* [ ] Assigns static routes
* [ ] Enables EIGRP on matching interfaces
* [ ] Defines the neighbor router
* [ ] Sets bandwidth limits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enables EIGRP on matching interfaces
💡 The `network` command under EIGRP configuration activates the protocol on interfaces whose IP addresses fall within the specified range.

</details>

---

### 46. In EIGRP, a feasible successor is:

* [ ] A backup route that meets the feasibility condition
* [ ] The primary route in the routing table
* [ ] A router that is unreachable
* [ ] A router in a different autonomous system

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A backup route that meets the feasibility condition
💡 Feasible successors provide precomputed loop-free backup paths, allowing fast failover.

</details>

---

### 47. Which OSPF packet type is used to establish and maintain neighbor relationships?

* [ ] Database Description
* [ ] Hello
* [ ] Link-State Request
* [ ] Link-State Update

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hello
💡 Hello packets are exchanged periodically to discover neighbors, establish adjacencies, and maintain connectivity.

</details>

---

### 48. If an OSPF router ID is not manually configured, it is automatically selected based on:

* [ ] Lowest IP address on loopback interface
* [ ] Highest IP address on loopback interface
* [ ] MAC address
* [ ] Highest IP on an active interface

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Highest IP address on loopback interface
💡 If no loopback is configured, the highest active interface IP is used to assign a router ID.

</details>

---

### 49. Which statement about EIGRP summarization is true?

* [ ] Enabled by default on all interfaces
* [ ] Works only with IPv6
* [ ] Must be manually configured
* [ ] Not supported at all

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Must be manually configured
💡 Automatic summarization can be disabled; manual summarization allows control over route advertisement.

</details>

---

### 50. What is a major difference between IGRP and EIGRP?

* [ ] IGRP is classless, EIGRP is classful
* [ ] EIGRP supports VLSM, IGRP does not
* [ ] IGRP supports link-state updates
* [ ] EIGRP works only on static networks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EIGRP supports VLSM, IGRP does not
💡 EIGRP is classless, allowing variable-length subnet masks, while IGRP is classful.

</details>

---

### 51. In OSPF, what is the function of LSAs (Link-State Advertisements)?

* [ ] Provide ARP information
* [ ] Establish static routes
* [ ] Share routing information with neighbors
* [ ] Assign IP addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Share routing information with neighbors
💡 LSAs allow OSPF routers to exchange information about their links and topology so all routers have a synchronized view of the network.

</details>

---

### 52. How does OSPF handle routing between multiple areas?

* [ ] Using floating static routes
* [ ] Through the backbone area (Area 0)
* [ ] Using route maps
* [ ] Only via default routes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Through the backbone area (Area 0)
💡 All inter-area OSPF traffic must pass through Area 0, the backbone, ensuring loop-free routing between areas.

</details>

---

### 53. For a route to qualify as a feasible successor in EIGRP, which condition must be satisfied?

* [ ] It must have the highest bandwidth
* [ ] Its advertised distance < feasible distance of the successor
* [ ] It must be manually configured
* [ ] It must be directly connected

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Its advertised distance < feasible distance of the successor
💡 This feasibility condition ensures the backup route is loop-free and can be used immediately if the primary fails.

</details>

---

### 54. What happens if OSPF routers in the same area have mismatched Hello and Dead intervals?

* [ ] They form an adjacency
* [ ] They form a neighbor relationship
* [ ] They will not become neighbors
* [ ] They will use default timers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They will not become neighbors
💡 OSPF requires identical Hello and Dead intervals to establish neighbor adjacencies; mismatched timers prevent adjacency formation.

</details>

---

### 55. Which EIGRP packet type is used to acknowledge the receipt of reliable messages?

* [ ] Hello
* [ ] Acknowledgment
* [ ] Update
* [ ] Query

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Acknowledgment
💡 EIGRP uses reliable transport with explicit acknowledgment packets to confirm receipt of updates and queries.

</details>

---

### 56. What is the default OSPF cost of a 100 Mbps FastEthernet interface?

* [ ] 1
* [ ] 10
* [ ] 100
* [ ] 1000

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1
💡 OSPF calculates cost as 100 Mbps / interface bandwidth (in Mbps). For 100 Mbps, cost = 100/100 = 1.

</details>

---

### 57. How does EIGRP provide loop-free paths during convergence?

* [ ] Through TTL
* [ ] By using Split Horizon
* [ ] Using the feasibility condition and DUAL
* [ ] Through shortest-path-first algorithm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Using the feasibility condition and DUAL
💡 EIGRP ensures loop-free paths using DUAL calculations and the feasibility condition, unlike simple distance-vector protocols.

</details>

---

### 58. Which type of OSPF LSA is originated by an ABR to describe routes between areas?

* [ ] Type 1
* [ ] Type 2
* [ ] Type 3
* [ ] Type 5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Type 3
💡 ABRs generate Type 3 LSAs (Summary LSAs) to advertise inter-area routes to other OSPF areas.

</details>

---

### 59. What is the main advantage of OSPF over distance-vector protocols like RIP?

* [ ] Simpler configuration
* [ ] Lower memory usage
* [ ] Faster convergence and loop prevention
* [ ] Broadcast-based routing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Faster convergence and loop prevention
💡 OSPF uses link-state information and SPF calculations for faster, loop-free routing, making it more suitable for large, dynamic networks.

</details>

---

### 60. What is the primary function of a Layer 2 switch?

* [ ] Routing packets between different networks
* [ ] Forwarding frames based on MAC addresses
* [ ] Translating IP addresses
* [ ] Encrypting data on the network

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forwarding frames based on MAC addresses
💡 Layer 2 switches operate at the data link layer, forwarding frames based on MAC addresses to reduce collisions and increase network efficiency.

</details>

---

### 61. What does STP stand for?

* [ ] Simple Transmission Protocol
* [ ] Spanning Tree Protocol
* [ ] Secure Transfer Protocol
* [ ] Switching Tree Process

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Spanning Tree Protocol
💡 STP prevents switching loops in Layer 2 networks by selectively blocking redundant paths and creating a loop-free topology.

</details>

---

### 62. Which device operates primarily at Layer 2 of the OSI model?

* [ ] Router
* [ ] Switch
* [ ] Hub
* [ ] Firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Switch
💡 Switches forward frames based on MAC addresses (Layer 2), while routers operate at Layer 3 using IP addresses.

</details>

---

### 63. What is the default STP protocol used in Cisco switches?

* [ ] RSTP
* [ ] PVST+
* [ ] MSTP
* [ ] STP (802.1D)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** STP (802.1D)
💡 Cisco switches historically use 802.1D STP by default, though PVST+ and RSTP are commonly enabled for faster convergence.

</details>

---

### 64. Which address type does a switch use to forward frames?

* [ ] IP address
* [ ] MAC address
* [ ] Port number
* [ ] Subnet mask

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MAC address
💡 Layer 2 switches use MAC addresses to decide the destination port for each frame.

</details>

---

### 65. What happens if there are redundant Layer 2 paths without STP?

* [ ] Faster data transfer
* [ ] Broadcast storms
* [ ] Increased bandwidth
* [ ] IP routing loops

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Broadcast storms
💡 Redundant links cause frames to loop endlessly, creating broadcast storms and network congestion if STP is not enabled.

</details>

---

### 66. When STP is first enabled, what is the initial port state?

* [ ] Forwarding
* [ ] Blocking
* [ ] Listening
* [ ] Disabled

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Blocking
💡 Ports start in the Blocking state to prevent loops until STP determines the correct topology.

</details>

---

### 67. What is the purpose of the STP Root Bridge?

* [ ] Act as a gateway for all VLANs
* [ ] Control Layer 3 routing decisions
* [ ] Provide a reference for path cost calculations
* [ ] Assign IP addresses to switches

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provide a reference for path cost calculations
💡 The Root Bridge serves as the central reference point, helping switches determine the shortest path to forward frames.

</details>

---

### 68. How is the Root Bridge elected in STP?

* [ ] Switch with the highest MAC address
* [ ] Switch with the lowest Bridge ID
* [ ] Switch with the most ports
* [ ] Switch with the fastest CPU

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Switch with the lowest Bridge ID
💡 Bridge ID combines priority and MAC address. The switch with the lowest value becomes the Root Bridge.

</details>

---

### 69. What is the default Bridge Priority value in STP?

* [ ] 4096
* [ ] 32768
* [ ] 65535
* [ ] 0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 32768
💡 Cisco switches use a default priority of 32768. Lowering the priority increases the likelihood of a switch becoming the Root Bridge.

</details>

---

### 70. Which STP port state is responsible for forwarding frames?

* [ ] Blocking
* [ ] Listening
* [ ] Learning
* [ ] Forwarding

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forwarding
💡 Only ports in the Forwarding state send and receive normal data frames on the network.

</details>

---

### 71. What is the purpose of STP port cost?

* [ ] Determine the Root Bridge
* [ ] Calculate the best path to the Root Bridge
* [ ] Assign VLAN membership
* [ ] Detect duplicate MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Calculate the best path to the Root Bridge
💡 Port cost is based on bandwidth and helps STP select the least-cost path to the Root Bridge.

</details>

---

### 72. Which port role in STP forwards frames toward the Root Bridge?

* [ ] Root Port
* [ ] Designated Port
* [ ] Blocked Port
* [ ] Alternate Port

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root Port
💡 The Root Port is the switch port with the lowest path cost to the Root Bridge.

</details>

---

### 73. During the STP Listening state, what occurs?

* [ ] Port forwards data frames
* [ ] Port learns MAC addresses
* [ ] Port sends/receives BPDUs but does not learn MACs
* [ ] Port is disabled

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Port sends/receives BPDUs but does not learn MACs
💡 Listening ports participate in topology negotiation without forwarding frames.

</details>

---

### 74. How often are BPDUs sent by default in 802.1D STP?

* [ ] Every 1 second
* [ ] Every 2 seconds
* [ ] Every 5 seconds
* [ ] Every 10 seconds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Every 2 seconds
💡 BPDUs are sent by the Root Bridge every 2 seconds to maintain network topology information.

</details>

---

### 75. What improvement does RSTP offer over traditional STP?

* [ ] Supports VLANs
* [ ] Faster convergence
* [ ] Uses more CPU resources
* [ ] Uses multicast MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Faster convergence
💡 RSTP (802.1w) reduces convergence time from 30–50 seconds to a few seconds after topology changes.

</details>

---

### 76. In PVST+, how many spanning tree instances exist?

* [ ] One per switch
* [ ] One per VLAN
* [ ] One per port
* [ ] One per IP subnet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** One per VLAN
💡 PVST+ creates a separate spanning tree instance for each VLAN, allowing load balancing across multiple VLANs on redundant links.

</details>

---

### 77. Which RSTP port state corresponds to traditional STP’s Blocking state?

* [ ] Discarding
* [ ] Learning
* [ ] Forwarding
* [ ] Listening

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Discarding
💡 In RSTP, the Discarding state prevents loops by not forwarding frames or learning MAC addresses, replacing Blocking/Listening.

</details>

---

### 78. How can you manually change the Bridge Priority on a Cisco switch?

* [ ] `spanning-tree priority [value]`
* [ ] `bridge priority [value]`
* [ ] `switch priority [value]`
* [ ] `spanning-tree root-priority [value]`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `spanning-tree priority [value]`
💡 This command adjusts a switch’s priority to influence Root Bridge election. Lower values increase chances of being elected Root.

</details>

---

### 79. What is a common consequence of a switching loop in a Layer 2 network?

* [ ] Increased routing table size
* [ ] Broadcast storms causing network slowdown
* [ ] Faster packet forwarding
* [ ] Reduced IP fragmentation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Broadcast storms causing network slowdown
💡 Switching loops continuously replicate broadcast frames, overwhelming the network and causing significant performance degradation.

</details>

---

### 80. Which protocol is used to detect Layer 2 loops and prevent them?

* [ ] OSPF
* [ ] STP
* [ ] ARP
* [ ] ICMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** STP
💡 Spanning Tree Protocol detects and disables redundant Layer 2 paths to prevent loops and broadcast storms.

</details>

---

### 81. What is a Designated Port in STP?

* [ ] The port with the highest cost on a switch
* [ ] The port selected to forward frames towards the Root Bridge on a LAN segment
* [ ] The port connected to the Root Bridge
* [ ] The port that blocks redundant links

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The port selected to forward frames towards the Root Bridge on a LAN segment
💡 On each segment, the Designated Port forwards frames to ensure connectivity toward the Root Bridge while preventing loops.

</details>

---

### 82. What does the Bridge ID (BID) in STP consist of?

* [ ] Switch MAC address only
* [ ] Bridge Priority and MAC address
* [ ] VLAN ID and MAC address
* [ ] Root ID and Port number

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bridge Priority and MAC address
💡 BID uniquely identifies a switch in STP and is used in Root Bridge election. Lower priority values are preferred.

</details>

---

### 83. How does MSTP improve upon PVST+ and RSTP?

* [ ] Allows multiple VLANs to map to a single spanning tree instance
* [ ] Supports faster convergence than RSTP
* [ ] Disables blocking ports automatically
* [ ] Uses the lowest MAC address for root bridge election

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Allows multiple VLANs to map to a single spanning tree instance
💡 MSTP reduces overhead in networks with many VLANs by grouping VLANs into instances instead of running one STP per VLAN.

</details>

---

### 84. What is the role of a Backup Port in STP?

* [ ] Forwards frames to the Root Bridge
* [ ] Provides a backup to the Designated Port on a shared segment
* [ ] Disabled for security reasons
* [ ] Connects directly to the Root Bridge

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provides a backup to the Designated Port on a shared segment
💡 A Backup Port is ready to take over if the Designated Port fails, ensuring redundancy on a LAN segment.

</details>

---

### 85. In STP, what is the purpose of the Max Age timer?

* [ ] Determines how long a switch keeps MAC address entries
* [ ] Defines how long a switch waits before declaring a BPDU stale
* [ ] Sets the interval for sending Hello messages
* [ ] Sets the interval for aging ARP entries

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Defines how long a switch waits before declaring a BPDU stale
💡 The Max Age timer prevents switches from using outdated topology information, maintaining loop-free operation.

</details>

---

### 86. What does the PortFast feature do in Cisco switches?

* [ ] Allows ports to bypass Listening and Learning states
* [ ] Increases the STP Hello interval
* [ ] Disables STP on the port
* [ ] Forces a port into Blocking mode

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Allows ports to bypass Listening and Learning states
💡 PortFast speeds up port activation for end devices by immediately transitioning to Forwarding, while still participating in STP protection mechanisms.

</details>

---

### 87. How does BPDU Guard improve network stability?

* [ ] Prevents ports from sending BPDUs
* [ ] Disables a port that receives a BPDU when PortFast is enabled
* [ ] Increases the Max Age timer
* [ ] Blocks Root Bridge election

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Disables a port that receives a BPDU when PortFast is enabled
💡 BPDU Guard protects against accidental loops caused by misconfigured devices on access ports configured with PortFast.

</details>

---

### 88. How does EtherChannel affect STP operation?

* [ ] STP treats all aggregated links as a single logical link
* [ ] STP disables EtherChannel
* [ ] STP blocks all but one link in EtherChannel
* [ ] EtherChannel does not interact with STP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** STP treats all aggregated links as a single logical link
💡 EtherChannel bundles multiple physical links into one logical link, preventing STP from blocking redundant physical connections unnecessarily.

</details>

---

### 89. Which of the following describes the concept of Root Guard?

* [ ] Prevents a switch from becoming the Root Bridge
* [ ] Protects the Root Bridge from being attacked by hackers
* [ ] Blocks ports that receive superior BPDUs to enforce Root Bridge location
* [ ] Speeds up STP convergence on Root ports

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Blocks ports that receive superior BPDUs to enforce Root Bridge location
💡 Root Guard ensures that designated Root Bridge placement is maintained by preventing unexpected root elections from other switches.

</details>

---

### 90. What is the primary purpose of a VLAN?

* [ ] To increase the number of IP addresses
* [ ] To segment a network into smaller broadcast domains
* [ ] To route traffic between different networks
* [ ] To encrypt data on the network

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To segment a network into smaller broadcast domains
💡 VLANs reduce broadcast traffic and improve network efficiency by logically dividing a single physical network into multiple isolated domains.

</details>

---

### 91. On which OSI layer do VLANs operate?

* [ ] Layer 1
* [ ] Layer 2
* [ ] Layer 3
* [ ] Layer 4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Layer 2
💡 VLANs operate at Layer 2 (Data Link), logically segmenting the network based on switch ports rather than IP addresses.

</details>

---

### 92. Which device typically supports VLAN configurations?

* [ ] Router
* [ ] Hub
* [ ] Switch
* [ ] Firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Switch
💡 Managed switches support VLANs, allowing segmentation of traffic and enhanced control over broadcast domains.

</details>

---

### 93. What VLAN ID number range is considered normal-range VLANs?

* [ ] 1 to 100
* [ ] 1 to 1005
* [ ] 1006 to 4094
* [ ] 4095 to 65535

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1 to 1005
💡 Normal-range VLANs include IDs 1–1005. VLANs 1006–4094 are extended VLANs used for large-scale networks.

</details>

---

### 94. What is the default VLAN on most Cisco switches?

* [ ] VLAN 0
* [ ] VLAN 1
* [ ] VLAN 10
* [ ] VLAN 100

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLAN 1
💡 All switch ports are assigned to VLAN 1 by default unless reconfigured. VLAN 1 also carries management traffic unless changed.

</details>

---

### 95. Which VLAN type carries traffic for multiple VLANs across a trunk link?

* [ ] Access VLAN
* [ ] Native VLAN
* [ ] Management VLAN
* [ ] Trunk VLAN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Trunk VLAN
💡 Trunk ports carry traffic for multiple VLANs using tagging (802.1Q) to distinguish VLANs.

</details>

---

### 96. What is the function of an access port on a switch?

* [ ] To carry traffic for multiple VLANs
* [ ] To connect end devices to a single VLAN
* [ ] To route between VLANs
* [ ] To encrypt VLAN traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To connect end devices to a single VLAN
💡 Access ports belong to a single VLAN and forward untagged traffic to that VLAN.

</details>

---

### 97. What protocol is used to negotiate trunk links between switches?

* [ ] CDP
* [ ] VTP
* [ ] DTP
* [ ] STP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DTP (Dynamic Trunking Protocol)
💡 DTP allows Cisco switches to automatically negotiate trunking and encapsulation (802.1Q or ISL) on point-to-point links.

</details>

---

### 98. Which VLAN is used by default for untagged traffic on a trunk port?

* [ ] VLAN 1
* [ ] Native VLAN
* [ ] VLAN 100
* [ ] Management VLAN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Native VLAN
💡 Untagged traffic on a trunk port is assigned to the Native VLAN. By default, this is VLAN 1 unless reconfigured.

</details>

---

### 99. What command enables a trunk link on a Cisco switch interface?

* [ ] `switchport mode access`
* [ ] `switchport mode trunk`
* [ ] `switchport trunk enable`
* [ ] `switchport trunk allowed vlan`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `switchport mode trunk`
💡 This command configures a switch interface to carry multiple VLANs as a trunk port.

</details>

---

### 100. What is the purpose of the Native VLAN on a trunk port?

* [ ] To carry tagged frames
* [ ] To carry untagged frames
* [ ] To assign IP addresses
* [ ] To filter VLAN traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To carry untagged frames
💡 Native VLAN ensures backward compatibility with devices that do not support VLAN tagging. Untagged frames are assigned to this VLAN.

</details>

---

### 101. Which VLAN range is considered extended VLANs?

* [ ] 1 to 1005
* [ ] 1006 to 4094
* [ ] 4095 to 5000
* [ ] 5001 to 65535

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1006 to 4094
💡 Extended VLANs are used in large networks and require VTP version 3 for propagation across switches.

</details>

---

### 102. What does VTP stand for?

* [ ] VLAN Trunk Protocol
* [ ] Virtual Trunk Protocol
* [ ] VLAN Transfer Protocol
* [ ] Virtual LAN Trunking Protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLAN Trunking Protocol
💡 VTP allows switches to share VLAN configuration information across a network, simplifying VLAN management.

</details>

---

### 103. What is the primary function of VTP?

* [ ] To route traffic between VLANs
* [ ] To synchronize VLAN information across switches
* [ ] To encrypt VLAN traffic
* [ ] To block VLAN loops

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To synchronize VLAN information across switches
💡 VTP ensures consistent VLAN configuration across multiple switches in the same VTP domain.

</details>

---

### 104. Which VTP mode allows VLAN creation, deletion, and advertisement?

* [ ] Client
* [ ] Server
* [ ] Transparent
* [ ] Off

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server
💡 VTP Server mode allows switches to create, modify, and advertise VLANs to clients in the same domain.

</details>

---

### 105. What happens when two switches have different VTP domain names?

* [ ] VLAN information is synchronized
* [ ] VLAN information is ignored
* [ ] VLAN information is deleted
* [ ] VLAN information is corrupted

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLAN information is ignored
💡 VTP messages are only accepted from switches within the same domain to prevent misconfiguration.

</details>

---

### 106. Which type of VLAN is used to separate management traffic from user data?

* [ ] Native VLAN
* [ ] Default VLAN
* [ ] Management VLAN
* [ ] Data VLAN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Management VLAN
💡 Management VLANs isolate switch management traffic from regular user traffic for enhanced security.

</details>

---

### 107. How many VLANs can be supported in a standard VLAN implementation?

* [ ] 64
* [ ] 256
* [ ] 4094
* [ ] 65535

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 4094
💡 Standard VLAN IDs range from 1 to 4094 (1–1005 normal range, 1006–4094 extended range).

</details>

---

### 108. What encapsulation types are supported on Cisco trunk ports?

* [ ] ISL and 802.1Q
* [ ] VLAN and STP
* [ ] CDP and VTP
* [ ] DTP and STP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ISL and 802.1Q
💡 802.1Q is the industry standard, while ISL is Cisco proprietary, both used for tagging VLANs on trunk links.

</details>

---

### 109. Which VLAN is typically excluded from trunking?

* [ ] VLAN 1
* [ ] Native VLAN
* [ ] Management VLAN
* [ ] Data VLAN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLAN 1
💡 VLAN 1 is often excluded from trunking to enhance security and prevent potential VLAN hopping attacks.

</details>

---

### 110. What command displays VLANs configured on a Cisco switch?

* [ ] `show vlan`
* [ ] `show ip vlan`
* [ ] `show vlan brief`
* [ ] `show trunk`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `show vlan brief`
💡 This command provides a concise view of all VLANs configured on the switch, their status, and associated ports.

</details>

---

### 111. What is the function of a VLAN Access Control List (VACL)?

* [ ] To route VLAN traffic
* [ ] To filter traffic within a VLAN
* [ ] To create VLANs
* [ ] To assign VLAN IDs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To filter traffic within a VLAN
💡 VACLs allow administrators to enforce security policies by controlling traffic between devices within the same VLAN.

</details>

---

### 112. How does VTP pruning improve network performance?

* [ ] By increasing VLAN numbers
* [ ] By reducing unnecessary VLAN traffic on trunk links
* [ ] By encrypting VLAN data
* [ ] By blocking VLANs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** By reducing unnecessary VLAN traffic on trunk links
💡 VTP pruning prevents traffic for VLANs that do not exist on a downstream switch from being sent over the trunk, saving bandwidth.

</details>

---

### 113. What is the default VTP version on Cisco switches?

* [ ] Version 1
* [ ] Version 2
* [ ] Version 3
* [ ] Version 4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Version 1
💡 VTP version 1 is the default, supporting normal VLANs but not extended VLANs; version 3 is required for extended VLANs.

</details>

---

### 114. What happens to VLAN information on a switch configured in VTP Transparent mode?

* [ ] VLANs are synchronized across the domain
* [ ] VLANs are not advertised but are locally maintained
* [ ] VLANs are deleted automatically
* [ ] VLANs are shared with clients only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VLANs are not advertised but are locally maintained
💡 Transparent mode allows local VLAN configuration without affecting other switches in the VTP domain.

</details>

---

### 115. Which VTP version supports extended VLANs?

* [ ] Version 1
* [ ] Version 2
* [ ] Version 3
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Version 3
💡 VTP version 3 supports extended VLANs (1006–4094), enhanced authentication, and primary server designation.

</details>

---

### 116. What is a common cause of VLAN mismatch errors between switches?

* [ ] Different native VLANs on trunk ports
* [ ] Different IP addresses
* [ ] Different spanning tree versions
* [ ] Different MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Different native VLANs on trunk ports
💡 Native VLAN mismatches prevent untagged frames from reaching the correct VLAN, causing connectivity issues.

</details>

---

### 117. Which VLAN type cannot be deleted on a Cisco switch?

* [ ] Native VLAN
* [ ] Default VLAN (VLAN 1)
* [ ] Management VLAN
* [ ] Extended VLAN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Default VLAN (VLAN 1)
💡 VLAN 1 is built-in and cannot be deleted, though it can be reassigned for management or trunk purposes.

</details>

---

### 118. What does a VLAN hopping attack exploit?

* [ ] Weak passwords
* [ ] Misconfigured VLAN trunking
* [ ] Outdated firmware
* [ ] Unencrypted VLAN traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Misconfigured VLAN trunking
💡 Attackers exploit improperly configured trunk ports to send traffic to VLANs they should not access.

</details>

---

### 119. How can VLAN hopping attacks be prevented?

* [ ] Disable unused ports and assign them to unused VLANs
* [ ] Use VTP in server mode
* [ ] Use VLAN 1 for all ports
* [ ] Enable port security on trunk ports

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Disable unused ports and assign them to unused VLANs
💡 Proper port configuration and VLAN assignment prevent attackers from exploiting VLAN hopping vulnerabilities.

</details>

---

### 120. What is the main purpose of port security on a switch?

* [ ] To increase network speed
* [ ] To limit the number of MAC addresses on a port
* [ ] To assign IP addresses
* [ ] To encrypt data

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To limit the number of MAC addresses on a port
💡 Port security prevents unauthorized devices from connecting by restricting the number of MAC addresses allowed on a switch port.

</details>

---

### 121. Which type of attack can port security help prevent?

* [ ] Phishing
* [ ] MAC address flooding
* [ ] DNS spoofing
* [ ] SQL injection

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MAC address flooding
💡 Attackers attempting to overflow a switch’s MAC table are blocked by port security, preventing network-wide broadcast flooding.

</details>

---

### 122. What does an Access Control List (ACL) primarily do?

* [ ] Encrypts network traffic
* [ ] Filters network traffic based on rules
* [ ] Routes traffic between VLANs
* [ ] Manages IP addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Filters network traffic based on rules
💡 ACLs define explicit rules to permit or deny traffic based on source/destination IPs, protocols, or ports.

</details>

---

### 123. Which protocol is commonly used for device authentication in AAA?

* [ ] FTP
* [ ] TACACS+
* [ ] HTTP
* [ ] SMTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TACACS+
💡 TACACS+ provides centralized authentication, authorization, and accounting for network devices and encrypts the entire payload.

</details>

---

### 124. What is the default action of an ACL if no rule matches?

* [ ] Permit the traffic
* [ ] Deny the traffic
* [ ] Redirect the traffic
* [ ] Log the traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deny the traffic
💡 ACLs have an implicit “deny all” rule at the end, so any unmatched traffic is blocked by default.

</details>

---

### 125. Which IPv4 ACL statement would block traffic from IP 192.168.1.10?

* [ ] `permit ip host 192.168.1.10 any`
* [ ] `deny ip host 192.168.1.10 any`
* [ ] `deny ip any host 192.168.1.10`
* [ ] `permit ip any any`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `deny ip host 192.168.1.10 any`
💡 This statement denies all traffic originating from 192.168.1.10 to any destination.

</details>

---

### 126. What is the purpose of device hardening?

* [ ] To speed up device performance
* [ ] To secure devices by reducing vulnerabilities
* [ ] To increase device storage
* [ ] To configure VLANs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To secure devices by reducing vulnerabilities
💡 Hardening involves disabling unused services, changing default passwords, and applying security policies to protect network devices.

</details>

---

### 127. How does port security handle a violation by default?

* [ ] Shut down the port
* [ ] Ignore the violation
* [ ] Send a warning only
* [ ] Reboot the switch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Shut down the port
💡 Default violation mode (shutdown) disables the port immediately to prevent unauthorized access.

</details>

---

### 128. Which of the following is NOT a common port security violation mode?

* [ ] Protect
* [ ] Restrict
* [ ] Notify
* [ ] Shutdown

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Notify
💡 Cisco switches support Protect, Restrict, and Shutdown modes. “Notify” is not a standard violation mode.

</details>

---

### 129. Which IPv6 ACL keyword is used to specify a source address?

* [ ] src
* [ ] from
* [ ] ipv6 address
* [ ] source

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** src
💡 The `src` keyword in IPv6 ACLs specifies the source IPv6 address to permit or deny traffic.

</details>

---

### 130. What is the purpose of the APIC-EM Path Trace tool?

* [ ] To configure VLANs
* [ ] To trace the path of network traffic and verify ACLs
* [ ] To assign IP addresses
* [ ] To encrypt traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To trace the path of network traffic and verify ACLs
💡 APIC-EM Path Trace allows network administrators to simulate and verify traffic flow between endpoints, ensuring policies and ACLs function correctly.

</details>

---

### 131. What is the difference between TACACS+ and RADIUS in AAA?

* [ ] TACACS+ encrypts the entire packet; RADIUS encrypts only the password
* [ ] RADIUS encrypts the entire packet; TACACS+ encrypts only the password
* [ ] TACACS+ is for IPv6 only; RADIUS is for IPv4 only
* [ ] There is no difference

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TACACS+ encrypts the entire packet; RADIUS encrypts only the password
💡 TACACS+ provides better security for administrative access by encrypting the full payload, while RADIUS only encrypts credentials.

</details>

---

### 132. Which device hardening step helps prevent unauthorized remote access?

* [ ] Enable telnet
* [ ] Disable unused services
* [ ] Increase bandwidth
* [ ] Configure VLANs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Disable unused services
💡 Disabling unneeded services like telnet or HTTP reduces the attack surface and prevents unauthorized access.

</details>

---

### 133. What is the main benefit of using standard ACLs?

* [ ] They filter traffic based on source IP only
* [ ] They filter traffic based on destination IP only
* [ ] They filter traffic based on protocol type
* [ ] They encrypt traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They filter traffic based on source IP only
💡 Standard ACLs provide basic control by permitting or denying traffic based solely on source IP addresses.

</details>

---

### 134. Extended ACLs differ from standard ACLs because they:

* [ ] Can filter by source and destination IP and protocol
* [ ] Are simpler to configure
* [ ] Filter only by MAC addresses
* [ ] Are only for IPv6

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Can filter by source and destination IP and protocol
💡 Extended ACLs offer granular control, including source/destination IP, protocol type, and port numbers.

</details>

---

### 135. What command is used to enable port security on a Cisco switch interface?

* [ ] `switchport port-security`
* [ ] `enable port-security`
* [ ] `port-security enable`
* [ ] `security-port enable`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `switchport port-security`
💡 This command enables port security on a specific interface, allowing configuration of MAC address limits, violation modes, and sticky MAC addresses.

</details>

---

### 136. In an ACL, what does the keyword “any” specify?

* [ ] Any source IP address
* [ ] Any destination IP address
* [ ] Any protocol type
* [ ] Both any source and destination IP address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both any source and destination IP address
💡 Using `any` allows ACL rules to apply to all IP addresses unless further specified.

</details>

---

### 137. What is the main function of RADIUS in AAA?

* [ ] Authentication and accounting only
* [ ] Authentication, authorization, and accounting
* [ ] Authorization only
* [ ] Accounting only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication, authorization, and accounting
💡 RADIUS centralizes AAA services, often used for network access control and accounting for network usage.

</details>

---

### 138. Which ACL type can filter IPv6 traffic?

* [ ] Standard IPv4 ACL
* [ ] Extended IPv4 ACL
* [ ] Named IPv6 ACL
* [ ] MAC ACL

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Named IPv6 ACL
💡 IPv6 ACLs support filtering by source/destination IPv6 addresses, protocol types, and ports.

</details>

---

### 139. What is a common way to verify ACLs on a Cisco device?

* [ ] `show running-config`
* [ ] `show access-lists`
* [ ] `show interfaces`
* [ ] `show ip route`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `show access-lists`
💡 This command displays all configured ACLs along with their rules and hit counts, useful for troubleshooting.

</details>

---

### 140. What is the primary benefit of device hardening?

* [ ] To improve network speed
* [ ] To protect devices from security threats
* [ ] To enable automatic configuration
* [ ] To increase device memory

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To protect devices from security threats
💡 Device hardening reduces vulnerabilities by disabling unused services, enforcing strong passwords, and applying security policies.

</details>

---

### 141. What is the main advantage of TACACS+ over RADIUS for device administration?

* [ ] TACACS+ separates authentication, authorization, and accounting processes
* [ ] RADIUS separates authentication, authorization, and accounting processes
* [ ] TACACS+ supports only UDP protocol
* [ ] RADIUS supports encryption of the entire packet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TACACS+ separates authentication, authorization, and accounting processes
💡 TACACS+ provides more granular control for administrative access; each AAA function can be managed independently.

</details>

---

### 142. How can you troubleshoot a port security violation on a Cisco switch?

* [ ] Use the command `show port-security interface`
* [ ] Use `show vlan`
* [ ] Use `show mac address-table`
* [ ] Use `show running-config` only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use the command `show port-security interface`
💡 This command shows violation counts, MAC addresses, and security settings to help troubleshoot blocked ports.

</details>

---

### 143. When configuring IPv4 ACLs, what does the keyword “host” specify?

* [ ] A single IP address
* [ ] A range of IP addresses
* [ ] Any IP address
* [ ] The local device IP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A single IP address
💡 Using `host <IP>` matches only that exact IP address in ACL rules.

</details>

---

### 144. What is a key feature of the APIC-EM Path Trace tool related to ACLs?

* [ ] It applies ACL rules automatically
* [ ] It analyzes and verifies the effect of ACLs on a given network path
* [ ] It deletes unused ACLs
* [ ] It creates ACLs from templates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It analyzes and verifies the effect of ACLs on a given network path
💡 APIC-EM Path Trace helps administrators confirm that ACLs permit or deny traffic as intended.

</details>

---

### 145. Which command would create a named extended IPv6 ACL?

* [ ] `ipv6 access-list NAME`
* [ ] `access-list ipv6 NAME`
* [ ] `ipv6 acl NAME`
* [ ] `ipv6 filter NAME`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `ipv6 access-list NAME`
💡 This command creates a named IPv6 ACL, allowing configuration of specific permit/deny rules for traffic.

</details>

---

### 146. How does port security limit the number of MAC addresses on a port?

* [ ] By configuring a maximum number of allowed MAC addresses
* [ ] By encrypting MAC addresses
* [ ] By blocking all unknown MAC addresses permanently
* [ ] By changing MAC addresses automatically

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** By configuring a maximum number of allowed MAC addresses
💡 Administrators can define a limit; once exceeded, violation actions (shutdown, restrict, protect) are triggered.

</details>

---

### 147. What is the purpose of “sticky” MAC addresses in port security?

* [ ] To allow the switch to dynamically learn and save MAC addresses
* [ ] To block all MAC addresses except the default
* [ ] To permanently disable the port
* [ ] To increase port speed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To allow the switch to dynamically learn and save MAC addresses
💡 Sticky MAC addresses automatically populate the running configuration and persist across reboots if saved.

</details>

---

### 148. What is the primary function of AAA in network security?

* [ ] Allocate IP addresses
* [ ] Authenticate, authorize, and account for user access
* [ ] Filter IP traffic
* [ ] Encrypt data

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticate, authorize, and account for user access
💡 AAA ensures that only authenticated users can access network resources and tracks their activities.

</details>

---

### 149. Which protocol does TACACS+ use for communication?

* [ ] TCP
* [ ] UDP
* [ ] ICMP
* [ ] HTTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TCP
💡 TACACS+ uses TCP port 49 to ensure reliable delivery and full encryption of all communication between clients and servers.

</details>

---

### 150. Which AAA component is responsible for verifying user identity?

* [ ] Authentication
* [ ] Authorization
* [ ] Accounting
* [ ] Access control

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication
💡 Authentication confirms the identity of a user or device before granting access.

</details>

---

### 151. Which AAA component controls what actions a user can perform after logging in?

* [ ] Authentication
* [ ] Authorization
* [ ] Accounting
* [ ] Verification

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authorization
💡 Authorization determines privileges, such as which commands or network resources a user can access.

</details>

---

### 152. Which AAA component records user activity on network devices?

* [ ] Authentication
* [ ] Authorization
* [ ] Accounting
* [ ] Encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Accounting
💡 Accounting logs user activities, including login times, commands executed, and resource usage.

</details>

---

### 153. In TACACS+, which transport protocol ensures reliability and full packet encryption?

* [ ] TCP
* [ ] UDP
* [ ] ICMP
* [ ] HTTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TCP
💡 TACACS+ uses TCP (port 49) for reliable delivery and encrypts the entire payload for administrative security.

</details>

---

### 154. Which protocol typically encrypts only user passwords in AAA communications?

* [ ] TACACS+
* [ ] RADIUS
* [ ] SNMPv3
* [ ] HTTPS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RADIUS
💡 RADIUS encrypts only the password field; other data like username and commands are sent in cleartext.

</details>

---

### 155. Which port security violation mode allows traffic from known MAC addresses but drops unknown ones without shutting down the port?

* [ ] Protect
* [ ] Restrict
* [ ] Shutdown
* [ ] Notify

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Protect
💡 The Protect mode drops packets from unknown MACs silently without incrementing violation counters or shutting the port.

</details>

---

### 156. Which port security violation mode sends a log message and increments the violation counter while still allowing traffic from known MACs?

* [ ] Protect
* [ ] Restrict
* [ ] Shutdown
* [ ] Block

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Restrict
💡 Restrict mode notifies administrators and tracks violations but does not shut the port down.

</details>

---

### 157. In port security, which feature allows a dynamically learned MAC address to persist across reboots?

* [ ] Sticky MAC addresses
* [ ] Static MAC addresses
* [ ] Dynamic MAC addresses
* [ ] Floating MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Sticky MAC addresses
💡 Sticky MAC addresses are dynamically learned and automatically added to the running configuration, saving them permanently when the config is saved.

</details>

---

### 158. What is the main function of a RADIUS server in network AAA?

* [ ] Authenticate, authorize, and account for users accessing network services
* [ ] Provide firewall services
* [ ] Encrypt VLAN traffic
* [ ] Assign IP addresses dynamically

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticate, authorize, and account for users accessing network services
💡 RADIUS centralizes AAA for network access, commonly used with VPNs, wireless networks, and 802.1X authentication.

</details>

---

### 159. What is the difference between TACACS+ and RADIUS in terms of encryption?

* [ ] TACACS+ encrypts the entire payload; RADIUS encrypts only passwords
* [ ] RADIUS encrypts the entire payload; TACACS+ encrypts only passwords
* [ ] Both encrypt only passwords
* [ ] Both encrypt the entire payload

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TACACS+ encrypts the entire payload; RADIUS encrypts only passwords
💡 TACACS+ is preferred for administrative access because all commands and credentials are encrypted, unlike RADIUS.

</details>

---

### 160. A company has a private IPv4 network and wants its devices to access the Internet without exposing internal addresses. Which technology should be implemented?

* [ ] Static routing
* [ ] NAT
* [ ] VLAN
* [ ] ACL

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NAT
💡 Network Address Translation (NAT) allows private IP addresses to communicate with public networks by translating private addresses to public IPs. This is standard practice for Internet connectivity of internal networks.

</details>

---

### 161. Which IPv6 address type is designed for use within private networks and is not globally routable?

* [ ] Global unicast
* [ ] Link-local
* [ ] Unique local
* [ ] Anycast

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Unique local
💡 Unique Local Addresses (ULAs, fc00::/7) are equivalent to private IPv4 addresses and are routable only within private networks.

</details>

---

### 162. A network administrator wants all internal devices to access the Internet while using a single public IP. Which NAT variant should be used?

* [ ] Static NAT
* [ ] Dynamic NAT
* [ ] Port Address Translation (PAT)
* [ ] Overloaded NAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Port Address Translation (PAT)
💡 PAT maps multiple private IP addresses to a single public IP using different port numbers, enabling many-to-one translation.

</details>

---

### 163. What is the fixed length of an IPv6 address and why is it significant compared to IPv4?

* [ ] 32 bits, allows fewer hosts per network
* [ ] 64 bits, designed for subnetting flexibility
* [ ] 128 bits, supports a vastly larger address space
* [ ] 256 bits, future-proofing the Internet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 128 bits
💡 IPv6 addresses are 128 bits long, providing a virtually unlimited number of unique addresses compared to IPv4’s 32-bit addressing.

</details>

---

### 164. A WAN link requires a dedicated, guaranteed bandwidth for an enterprise. Which technology fits this requirement?

* [ ] DSL
* [ ] Frame Relay
* [ ] T1 leased line
* [ ] LTE

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** T1 leased line
💡 A T1 line is a dedicated point-to-point leased line offering fixed bandwidth, reliability, and low latency suitable for enterprise WAN connections.

</details>

---

### 165. In IPv6, what does the address notation ::/0 represent in routing tables?

* [ ] Loopback
* [ ] Default route
* [ ] Localhost
* [ ] Multicast

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Default route
💡 ::/0 is the IPv6 default route, matching all destinations not explicitly found in the routing table, similar to 0.0.0.0/0 in IPv4.

</details>

---

### 166. Which protocol is commonly used to establish DSL connections requiring authentication?

* [ ] PPPoE
* [ ] RIP
* [ ] BGP
* [ ] SMTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PPPoE
💡 Point-to-Point Protocol over Ethernet (PPPoE) is used by DSL to encapsulate PPP frames over Ethernet and perform authentication for WAN access.

</details>

---

### 167. Which NAT type assigns a private IP a dedicated public IP permanently?

* [ ] Dynamic NAT
* [ ] Static NAT
* [ ] PAT
* [ ] SNAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Static NAT
💡 Static NAT maps one private IP to one public IP consistently, ensuring predictable address translation for services like servers.

</details>

---

### 168. On a Cisco router, which command shows active NAT translations?

* [ ] show ip route
* [ ] show interfaces
* [ ] show ip nat translations
* [ ] show ip protocols

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** show ip nat translations
💡 This command displays the current NAT table entries, showing which internal addresses map to which external addresses.

</details>

---

### 169. What differentiates PAT from Static NAT in terms of address mapping?

* [ ] PAT uses multiple public IPs per private IP
* [ ] PAT maps many-to-one using port numbers
* [ ] PAT maps one-to-one
* [ ] Static NAT is dynamic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PAT maps many-to-one using port numbers
💡 PAT allows multiple private IPs to share a single public IP by differentiating traffic using source port numbers.

</details>

---

### 170. Which IPv6 address is automatically assigned to every interface for communication on the same link?

* [ ] ff00::/8
* [ ] fe80::/10
* [ ] fc00::/7
* [ ] 2001::/16

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** fe80::/10
💡 Link-local addresses (fe80::/10) are automatically assigned to interfaces and used for communication within the same link only.

</details>

---

### 171. Which WAN technology transmits data in fixed-size cells rather than variable-length packets?

* [ ] ATM
* [ ] Frame Relay
* [ ] MPLS
* [ ] ISDN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ATM
💡 Asynchronous Transfer Mode (ATM) uses fixed 53-byte cells, enabling predictable latency and QoS in WAN networks.

</details>

---

### 172. What is the standard Maximum Transmission Unit (MTU) size for Ethernet networks over WAN?

* [ ] 1024 bytes
* [ ] 1280 bytes
* [ ] 1500 bytes
* [ ] 2048 bytes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1500 bytes
💡 Ethernet frames have a default MTU of 1500 bytes, ensuring compatibility and efficient transmission across WAN links.

</details>

---

### 173. Which technology allows secure communication over a public WAN without a dedicated leased line?

* [ ] DSL
* [ ] VPN
* [ ] MPLS
* [ ] ATM

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VPN
💡 Virtual Private Networks (VPNs) use encryption and tunneling to create secure connections over public networks like the Internet.

</details>

---

### 174. How many bits does each group (hextet) in an IPv6 address contain?

* [ ] 4 bits
* [ ] 8 bits
* [ ] 16 bits
* [ ] 32 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 16 bits
💡 Each of the eight groups in an IPv6 address (hextet) is 16 bits, represented as four hexadecimal digits.

</details>

---

### 175. Which NAT type allows multiple private IPs to share a single public IP using different ports?

* [ ] Static NAT
* [ ] Port Address Translation (PAT)
* [ ] Dynamic NAT
* [ ] Overloaded NAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Port Address Translation (PAT)
💡 PAT enables many-to-one IP translation by using port numbers to distinguish connections.

</details>

---

### 176. Which protocol is commonly used to establish WAN connections with username/password authentication?

* [ ] RIP
* [ ] PPP
* [ ] EIGRP
* [ ] SMTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PPP
💡 Point-to-Point Protocol (PPP) is used in WANs to encapsulate packets and authenticate connections using PAP/CHAP.

</details>

---

### 177. Which packet-switched WAN technology uses virtual circuits to connect multiple sites?

* [ ] Leased Line
* [ ] Frame Relay
* [ ] DSL
* [ ] MPLS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Frame Relay
💡 Frame Relay is a packet-switched WAN technology that provides logical virtual circuits over shared networks.

</details>

---

### 178. Which IPv6 address type is used for one-to-many communication?

* [ ] Unicast
* [ ] Anycast
* [ ] Multicast
* [ ] Broadcast

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multicast
💡 Multicast addresses deliver packets from one sender to multiple receivers efficiently; IPv6 does not use broadcast.

</details>

---

### 179. How does NAT impact end-to-end IP traceability?

* [ ] Improves it
* [ ] No effect
* [ ] Disables it
* [ ] Enhances it

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Disables it
💡 NAT hides internal IP addresses, breaking direct end-to-end traceability, which can impact logging and security mechanisms.

</details>

---

### 180. A company wants to allow internal devices to access the Internet, but public IPs should be assigned dynamically from a pool. Which NAT type achieves this?

* [ ] PAT
* [ ] Static NAT
* [ ] Dynamic NAT
* [ ] Overloaded NAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamic NAT
💡 Dynamic NAT maps private IPs to public IPs dynamically from a defined pool. Unlike Static NAT, the mapping is not fixed, allowing flexible use of limited public addresses.

</details>

---

### 181. An organization is migrating to IPv6 but still needs to communicate with legacy IPv4 systems. Which transition mechanism encapsulates IPv6 packets inside IPv4 packets?

* [ ] Dual Stack
* [ ] NAT64
* [ ] Tunneling
* [ ] DHCPv6

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tunneling
💡 Tunneling (e.g., 6to4, ISATAP) encapsulates IPv6 packets in IPv4, enabling IPv6 traffic to traverse IPv4 infrastructure during the transition period.

</details>

---

### 182. In an IPv6-only network, which solution allows devices to access IPv4-only resources?

* [ ] Dual Stack
* [ ] NAT64
* [ ] Tunneling
* [ ] DHCPv6

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NAT64
💡 NAT64 enables IPv6-only hosts to communicate with IPv4 servers by translating IPv6 addresses into IPv4 addresses and vice versa.

</details>

---

### 183. A company wants multiple branch offices connected with a WAN technology that forwards packets based on labels instead of IP addresses. Which technology should be implemented?

* [ ] MPLS
* [ ] PPP
* [ ] ISDN
* [ ] ATM

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MPLS
💡 Multiprotocol Label Switching (MPLS) uses labels for routing instead of IP addresses, enabling faster and scalable WAN connections with QoS support.

</details>

---

### 184. What is the default administrative distance of a static route on a Cisco router, and why is it important?

* [ ] 1
* [ ] 90
* [ ] 110
* [ ] 120

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1
💡 Administrative distance (AD) determines route trustworthiness. Static routes have AD = 1, making them preferred over dynamically learned routes unless explicitly overridden.

</details>

---

### 185. In IPv6, which part of the address identifies the subnet?

* [ ] Interface ID
* [ ] Network prefix
* [ ] Host portion
* [ ] MAC address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network prefix
💡 The network prefix defines the subnet in IPv6, while the interface ID identifies individual hosts within that subnet.

</details>

---

### 186. Considering the IPv6 global unicast address space, how many unique addresses are theoretically possible?

* [ ] 2^32
* [ ] 2^64
* [ ] 2^128
* [ ] 2^96

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 2^128
💡 IPv6 uses 128-bit addressing, allowing 2^128 unique addresses, vastly expanding the address space compared to IPv4’s 32-bit scheme.

</details>

---

### 187. Which is a major security concern introduced by NAT in enterprise networks?

* [ ] NAT increases traffic delays
* [ ] NAT supports only TCP
* [ ] NAT breaks end-to-end IP traceability and encryption
* [ ] NAT only works with IPv6

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NAT breaks end-to-end IP traceability and encryption
💡 NAT obscures internal IP addresses, disrupting direct end-to-end IP traceability. It can also interfere with IPsec and other end-to-end encryption mechanisms.

</details>

---

### 188. In WAN deployments, which is the primary advantage of MPLS compared to traditional IP routing?

* [ ] Simplified network topology
* [ ] Cost-effective bandwidth
* [ ] Uses labels for faster packet forwarding
* [ ] Enforces shortest-path routing only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Uses labels for faster packet forwarding
💡 MPLS forwards packets based on labels rather than IP headers, reducing routing lookup time and enabling QoS, traffic engineering, and scalable VPNs.

</details>

---

### 189. A network engineer wants to identify the subnet portion in an IPv6 address fe80::1ff:fe23:4567:890a/64. Which portion represents the subnet?

* [ ] fe80::
* [ ] 1ff:fe23:4567:890a
* [ ] /64
* [ ] 890a

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /64
💡 In IPv6, the prefix length (here /64) determines the subnet. The first 64 bits are the network prefix, and the remaining 64 bits represent the interface ID.

</details>

---

### 190. In a point-to-point WAN link, which protocol is primarily used to encapsulate packets and can support multiple authentication mechanisms?

* [ ] Peer-to-Peer Protocol
* [ ] Public Packet Protocol
* [ ] Private Path Protocol
* [ ] Point-to-Point Protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Point-to-Point Protocol
💡 PPP (Point-to-Point Protocol) is a standard data link layer protocol used to establish a direct connection between two network nodes. It supports authentication (PAP, CHAP), compression, and multilink capabilities.

</details>

---

### 191. A network engineer wants to secure a PPP connection against replay attacks. Which authentication protocol should they configure?

* [ ] FTP
* [ ] CHAP
* [ ] SSH
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CHAP
💡 Challenge Handshake Authentication Protocol (CHAP) periodically verifies the identity of the peer using a three-way handshake and does not send passwords in plaintext, unlike PAP. FTP, SSH, and SNMP are unrelated to PPP authentication.

</details>

---

### 192. An organization has multiple low-speed PPP links between two routers. They want to increase throughput by combining these links into one logical connection. Which solution should be used?

* [ ] To monitor PPP links
* [ ] To combine multiple PPP links into one logical link
* [ ] To encrypt PPP traffic
* [ ] To convert serial to Ethernet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To combine multiple PPP links into one logical link
💡 Multilink PPP (MLPPP) allows several physical PPP links to be combined into a single logical channel, increasing bandwidth and providing load balancing.

</details>

---

### 193. Which Cisco IOS command correctly enables PPP encapsulation on a serial interface?

* [ ] encapsulation hdlc
* [ ] encapsulation ppp
* [ ] ip encapsulation ppp
* [ ] set ppp enable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** encapsulation ppp
💡 In Cisco IOS, the `encapsulation ppp` command configures the interface to use PPP as its Layer 2 protocol. `encapsulation hdlc` sets HDLC, while the others are invalid commands.

</details>

---

### 194. In tunneling scenarios, which option correctly defines GRE?

* [ ] Generic Routing Extension
* [ ] General Routing Encapsulation
* [ ] Generic Routing Encapsulation
* [ ] Global Routing Encapsulation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Generic Routing Encapsulation
💡 GRE is a tunneling protocol that encapsulates various network layer protocols inside IP tunnels. The other options are incorrect expansions.

</details>

---

### 195. For a GRE tunnel between two routers, which IP address is typically used as the source?

* [ ] MAC address
* [ ] Tunnel IP address
* [ ] Loopback address or physical interface IP
* [ ] DNS hostname

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Loopback address or physical interface IP
💡 GRE tunnels use an IP address reachable by the tunnel destination as the source. Loopback addresses are preferred for stability, as physical interface IPs may go down.

</details>

---

### 196. An ISP wants to provide PPP services over its Ethernet infrastructure for remote clients. Which technology should they deploy?

* [ ] It encrypts Ethernet frames
* [ ] It allows PPP connections over Ethernet
* [ ] It replaces IP
* [ ] It manages VLAN tagging

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It allows PPP connections over Ethernet
💡 PPPoE (PPP over Ethernet) enables the encapsulation of PPP frames within Ethernet frames, allowing users to connect via standard Ethernet while using PPP features like authentication.

</details>

---

### 197. Which PPP authentication protocol transmits credentials in plaintext, making it less secure?

* [ ] CHAP
* [ ] PAP
* [ ] EAP
* [ ] RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PAP
💡 Password Authentication Protocol (PAP) sends username and password in plaintext. CHAP uses encrypted challenges, and EAP/RSA are more secure methods.

</details>

---

### 198. On a Cisco router, which interface type is specifically used for configuring a PPPoE client?

* [ ] VLAN interface
* [ ] Loopback interface
* [ ] Dialer interface
* [ ] Tunnel interface

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dialer interface
💡 PPPoE clients in Cisco IOS are configured on dialer interfaces, which abstract PPP session control from physical interfaces. VLAN, loopback, and tunnel interfaces are used for different purposes.

</details>

---

### 199. Which command binds a PPPoE dialer interface to a specific Ethernet interface?

* [ ] dialer attach
* [ ] pppoe-client dial-pool-number
* [ ] connect pppoe dialer
* [ ] ip pppoe enable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** pppoe-client dial-pool-number
💡 This command associates the PPPoE dialer interface with an Ethernet dialer pool. `dialer attach` is invalid, and `ip pppoe enable` is deprecated.

</details>

---

### 200. On a PPPoE dialer interface, which command allows the interface to automatically obtain its IP address from the ISP?

* [ ] ip address dhcp
* [ ] ip address negotiated
* [ ] ip negotiate
* [ ] ip address dynamic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ip address negotiated
💡 `ip address negotiated` configures the interface to accept the IP address provided by the PPPoE server during session establishment. `ip address dhcp` is for regular Ethernet interfaces.

</details>

---
